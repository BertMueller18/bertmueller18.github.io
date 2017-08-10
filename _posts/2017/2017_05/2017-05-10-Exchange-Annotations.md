---
layout: post 
title:  "Exchange Annotations" 
date:   2017-05-10T17:23
categories: exchange migration crossforest sidhistory activedirectory powershell
link: http://bertmueller18.github.io/
tags:
  - links
ogtype: article 
---
## SID HISTORY: Fixing Exchange

Locate and repair AD user accounts with acl inheritance flag uncheck. This prevents Exchange service accounts from altering user object and breaks various admin tools. 
?
# Download and install Quest AD PowerShell addon
# http://www.quest.com/powershell/activeroles-server.aspx
 
# Dump AD acl permission inheritance status for email enabled accounts before change
````powershell
Get-QADUser -SizeLimit 0 | where {$_.primarysmtpaddress -ne $null}|Select-Object SamAccountName,Name,@{n='IncludeInheritablePermissions';e={!$_.DirectoryEntry.PSBase.ObjectSecurity.AreAccessRulesProtected}}| Export-Csv -Encoding unicode -NoTypeInformation adpermissions-inheritance-pre.csv

# Enable AD acl permission inheritance for email enabled accounts, otherwise attempts to alter mailbox permissions will fail
Get-QADUser -SizeLimit 0 | where {$_.primarysmtpaddress -ne $null -and $_.DirectoryEntry.PSBase.ObjectSecurity.AreAccessRulesProtected} | Set-QADObjectSecurity -UnLockInheritance
 
# Dump AD acl permission inheritance status for email enabled accounts after change
Get-QADUser -SizeLimit 0 | where {$_.primarysmtpaddress -ne $null}|Select-Object SamAccountName,Name,@{n='IncludeInheritablePermissions';e={!$_.DirectoryEntry.PSBase.ObjectSecurity.AreAccessRulesProtected}}| Export-Csv -Encoding unicode -NoTypeInformation adpermissions-inheritance-post.csv
````
Fix mailbox permissions. First we grant “NT AUTHORITY\SELF” full access to mailbox which is default for Exchange 2007 and newer versions. Then we delete any permissions granted to valid user but with invalid SID (via SIDhistory). Next same permissions are added back which causes Exchange to resolve correct SID and joins permissions in case user had different permissions via new SID and SIDhistory SID. Finally any ACLs with unresolvable SIDs are removed. 
?
````powershell
# Dump list of mailbox permissions including SIDs prior making any changes
Get-Mailbox -ResultSize unlimited | Get-MailboxPermission | Select Identity,User,@{Name='SID';Expression={$_.user.securityidentifier}},Deny,IsInherited,InheritanceType,@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}} | Export-Csv -Encoding unicode -NoTypeInformation mbpermissions-all-pre.csv
 
 
# Grant everyone access to their own mailbox, this is default with Exchange 2007 and newer but still sometimes wrong for older migrated accounts
Get-mailbox -resultsize unlimited | Add-ADPermission -User "NT AUTHORITY\SELF" -ExtendedRights "Send-as" | ft -autosize -wrap
Get-mailbox -resultsize unlimited | Add-MailboxPermission -user "NT AUTHORITY\SELF" -Accessrights FullAccess | ft -autosize -wrap
 
 
# Get list of mailbox permissions with old SIDs
$fixmbperm = Get-Mailbox -ResultSize Unlimited | Get-MailboxPermission | where {$_.IsInherited -eq $false -and $_.Deny -eq $false -and $_.user -like "MYCORP\*"} | where {$_.user.securityidentifier -notlike "S-1-5-21-1423493088-*"}
 
# Save old permissions to file for future reference
echo $fixmbperm | Select Identity,User,@{Name='SID';Expression={$_.user.securityidentifier}},@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}} | Export-Csv -Encoding unicode -NoTypeInformation mbpermissions-fix.csv
 
# Delete permissions WITHOUT confirmation
echo $fixmbperm | %{Remove-MailboxPermission -identity $_.identity -user $_.user -access $_.accessrights -confirm:$false}
 
# Restore permissions WITHOUT confirmation
echo $fixmbperm | %{Add-MailboxPermission -identity $_.identity -user $_.user -access $_.accessrights -confirm:$false}
 
# Cleanup variable
Remove-Variable fixmbperm
 
 
# Get list of mailbox permissions without matching AD account (SID only)
$badmbperm = Get-Mailbox -ResultSize Unlimited | Get-MailboxPermission | where {$_.IsInherited -eq $false -and $_.Deny -eq $false -and $_.user -like "S-1-5-21-*"}
 
# Save old permissions to file for future reference
echo $badmbperm | Select Identity,User,@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}} | Export-Csv -Encoding unicode -NoTypeInformation mbpermissions-bad.csv
 
# Delete permissions WITHOUT confirmation
echo $badmbperm | %{Remove-MailboxPermission -identity $_.identity -user $_.user -access $_.accessrights -confirm:$false}
 
# Cleanup variable
Remove-Variable badmbperm
````
 
# Dump list of mailbox permissions including SIDs after changes
Get-Mailbox -ResultSize unlimited | Get-MailboxPermission | Select Identity,User,@{Name='SID';Expression={$_.user.securityidentifier}},Deny,IsInherited,InheritanceType,@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}} | Export-Csv -Encoding unicode -NoTypeInformation mbpermissions-all-post.csv

Fix public folder permissions. Here we delete invalid ACLs. Then we delete valid ACLs and re-create them. Many folders had permission corruption preventing Outlook and Exchange Management Console from accessing permission settings entirely without this. 
?
# Dump all public folder permissions to file prior making any changes
get-publicfolder "\" -recurse -resultsize unlimited| get-publicfolderclientpermission | Select Identity,User,@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}} | Sort-Object Identity,User|Export-Csv -Encoding unicode -NoTypeInformation pfpermissions-all-pre.csv
 
 
# Get permissions granted for deleted accounts and accounts with mailbox deleted (disabled users)
$badpfperm = get-publicfolder "\" -recurse -resultsize unlimited | get-publicfolderclientpermission | where {$_.user -like "NT User:S-1-*" -or $_.user -like "NT User:MYCORP\*"} | Sort-Object Identity,User
 
# Store list of permissions we're about to delete in CSV file for future reference
echo $badpfperm | Select Identity,User,@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}} | Export-Csv -Encoding unicode -NoTypeInformation pfpermissions-bad.csv
 
# Delete outdated permissions WITHOUT confirmation
echo $badpfperm | %{remove-publicfolderclientpermission -identity $_.identity -user $_.user -access $_.accessrights -confirm:$false}
 
# Cleanup variable
Remove-Variable badpfperm
 
 
# Get all valid permissions granted (excluding Default and Anonymous)
$okpfperm = get-publicfolder "\" -recurse -resultsize unlimited| get-publicfolderclientpermission | where {$_.user -notlike "NT User:S-1-*" -and $_.user -notlike "NT User:MYCORP\*" -and $_.user -notlike "Default" -and $_.user -notlike "Anonymous"} | Sort-Object Identity,User
 
# Store list of permissions we're about to alter in CSV file for future reference
echo $okpfperm | Select Identity,User,@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}} | Export-Csv -Encoding unicode -NoTypeInformation pfpermissions-ok.csv
 
# Delete permissions WITHOUT confirmation
echo $okpfperm | %{remove-publicfolderclientpermission -identity $_.identity -user $_.user -access $_.accessrights -confirm:$false}
 
# Restore permissions WITHOUT confirmation
echo $okpfperm | %{add-publicfolderclientpermission -identity $_.identity -user $_.user -access $_.accessrights -confirm:$false}
 
# Cleanup variable
Remove-Variable okpfperm
 
 
# Dump all public folder permissions to file after making changes
get-publicfolder "\" -recurse -resultsize unlimited| get-publicfolderclientpermission | Select Identity,User,@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}} | Sort-Object Identity,User|Export-Csv -Encoding unicode -NoTypeInformation pfpermissions-all-post.csv

Fix distribution list permissions. 
?
# Dump list of distribution list permissions including SIDs prior making any changes
Get-DistributionGroup -ResultSize unlimited | Get-ADPermission | Select Identity,User,@{Name='SID';Expression={$_.user.securityidentifier}},Deny,IsInherited,InheritanceType,@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}},@{Name='Extended Rights';Expression={[string]::join(', ', $_.ExtendedRights)}} | Export-Csv -Encoding unicode -NoTypeInformation dlpermissions-all-pre.csv
 
# Get list of distribution list permissions with old SIDs
$fixdlperm = Get-DistributionGroup -ResultSize Unlimited | Get-ADPermission | where {$_.IsInherited -eq $false -and $_.Deny -eq $false -and $_.user -like "MYCORP\*"} | where {$_.user.securityidentifier -notlike "S-1-5-21-1423493088-*"}
 
# Save old permissions to file for future reference
echo $fixdlperm | Select Identity,User,@{Name='SID';Expression={$_.user.securityidentifier}},@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}},@{Name='Extended Rights';Expression={[string]::join(', ', $_.ExtendedRights)}} | Export-Csv -Encoding unicode -NoTypeInformation dlpermissions-fix.csv
 
# Split regular and extended access rights to different variables
$fixdlpermac = echo $fixdlperm | where {$_.accessrights -ne $null -and $_.ExtendedRights -eq $null}
$fixdlpermex = echo $fixdlperm | where {$_.ExtendedRights -ne $null}
 
# Delete permissions WITHOUT confirmation
# This fail due bug like feature in Remove-ADPremissions causing it to first resolve old SID to username and then trying to remove ACL using new SID... idiots.
#echo $fixdlpermac | %{Remove-ADPermission -identity $_.identity -user $_.user -access $_.accessrights -confirm:$false}
#echo $fixdlpermex | %{Remove-ADPermission -identity $_.identity -user $_.user -extendedrights $_.ExtendedRights -confirm:$false}
 
# Restore permissions WITHOUT confirmation
# Because you can't delete old SIDs this will add new ACL entries for same users with new SID leaving ghost SIDs after SID history is removed
echo $fixdlpermac | %{Add-ADPermission -identity $_.identity -user $_.user -access $_.accessrights -confirm:$false}
echo $fixdlpermex | %{Add-ADPermission -identity $_.identity -user $_.user -extendedrights $_.ExtendedRights -confirm:$false}
 
# If you get access denied errors from two commands above check permissions on AD, don't be surprised if they're completely messed up due to incorrectly made old migration projects
 
# Dump list of distribution list permissions including SIDs after making changes
Get-DistributionGroup -ResultSize unlimited | Get-ADPermission | Select Identity,User,@{Name='SID';Expression={$_.user.securityidentifier}},Deny,IsInherited,InheritanceType,@{Name='Access Rights';Expression={[string]::join(', ', $_.AccessRights)}},@{Name='Extended Rights';Expression={[string]::join(', ', $_.ExtendedRights)}} | Export-Csv -Encoding unicode -NoTypeInformation dlpermissions-all-post.csv
 
# Cleanup variable
Remove-Variable fixdlperm
Remove-Variable fixdlpermac
Remove-Variable fixdlpermex

## Export out-of-office (OOF) autoreplies from Exchange 2010 with Powershell
Quick and very dirty export out-of-office (OOF) autoreplies from Exchange 2010 with Powershell. 

get-mailbox -resultsize unlimited |
get-mailboxautoreplyconfiguration |
where {$_.autoreplystate -ne "disabled"} |
select identity,autoreplystate,starttime,endtime,@{NAME='InternalMessage';Expression={$_.InternalMessage -replace ("`n") -replace("</p","/<") -replace("<.*?>") -replace("&nbsp;","")  }},@{NAME='ExternalMessage';Expression={$_.InternalMessage -replace ("`n") -replace("</p","/<") -replace("<.*?>") -replace("&nbsp;","")  }} |
Export-Csv -Encoding unicode -NoTypeInformation outofoffice.csv
