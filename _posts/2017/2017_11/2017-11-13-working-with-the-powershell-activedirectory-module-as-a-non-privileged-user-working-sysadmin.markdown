---
layout: post 
title:  "Working With The PowerShell ActiveDirectory Module As A Non-Privileged User – Working Sysadmin" 
date:   2017-11-13T20:32:00.012Z 
categories: activedirectory powershell
link: http://www.workingsysadmin.com/working-with-the-powershell-activedirectory-module-as-a-non-privileged-user/ 
tags:
  - links
ogtype: article 
---

## Working With The PowerShell ActiveDirectory Module As A Non-Privileged User

October 25, 2017active directory, PowerShellactive directory, activedirectory, powershell, PSDefaultParameterValues
As a best practice, as an administrator you should have separate accounts for your normal activities (emails, IM, normal stuff) and your administrative activities (resetting passwords, creating new mailboxes, etc.). It’s obviously best not to log into your normal workstation as your administrative user. You’re also absolutely not supposed to remote desktop into a domain controller (or another server) just to launch a PowerShell console, import the ActiveDirectory module, and run your commands. Here’s  better way.


We’re going to leverage the $PSDefaultParameterValues built-in variable which allows you to specify default values for cmdlets every time you run them.

First, set up a variable to hold your credentials.

````powershell
PS> $acred = Get-Credential -Message 'Admin creds'
# Now, import the ActiveDirectory module.

PS> Import-Module ActiveDirectory
# And finally, a little something special.
PS> $PSDefaultParameterValues += @{ 'activedirectory:\*:Credential' = $acred }
````

I’m adding a value to my $PSDefaultParameterValues variable. What I’m saying is for all the cmdlets in the ActiveDirectory module, set the -Credential parameter equal to the $acred variable that I set first.

Now when I run any commands using the ActiveDirectory module, they’ll run the the administrative credentials I supplied, instead of the credentials I’m logged into the computer with.

Share: