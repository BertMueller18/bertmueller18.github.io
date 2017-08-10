---
layout: post 
title:  "Some useful queries to use in Powershell - Syst &amp; Deploy " 
date:   2017-03-25T16:34:56.685Z 
categories: powershell wmi query
link: http://www.systanddeploy.com/2016/08/some-useful-queries-to-use-in-powershell.html?utm_campaign=crowdfire&utm_content=crowdfire&utm_medium=social&utm_source=twitter 
tags:
  - links
ogtype: article 
---

> Some useful queries to use in Powershell

 Damien Van Robaeys   15:26 
 

In this post, I'll show you some WMI query that can be used with Powershell. It's not very technical but that can be useful.
In a  previous post I have shown you a tool, OEM Support page,  to display your system informations. 
The informations below are used in this tool.
Display the installed Antivirus
Display the UAC status
Display the default printer
Display the installed language packs
Display the Windows Defender status
Display the firewall status
Display the installed RAM size
List hard disk total and free size
Display the current timezone
Display the Internet Explorer version
Display the SCCM site code
In this post I use Get-WMIObject for my queries but you can also use Get-CIMInstance.
See here a post, from Maik Koster, that explained why you should use the CIM method.

Display installed Antivirus
1
2
3
4
$Antivirus_test  = "SELECT * FROM AntiVirusProduct" 
$Win_Antivirus_Test = gwmi -Namespace "root\SecurityCenter2" -Query $Antivirus_test  @psboundparameters 
write-host $Win_Antivirus_Test.displayname
McAfee VirusScan Enterprise

Display UAC status
1
2
3
4
5
6
7
8
9
10
$REG_UAC = gp -path registry::"HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
$UAC_State = $REG_UAC.EnableLUA
If ($UAC_State -eq "0")
 {
  write-host "Disbaled" -foregroundcolor "yellow"
 }
Else
 {
  write-host "Enabled" -foregroundcolor "green"
 } 

Display default printer
1
2
3
$Win32_Printer = gwmi -Query " SELECT * FROM Win32_Printer WHERE Default=$true"
write-host $Win32_Printer.name
PR001657

Display installed language packs
1
2
3
$Win32_OperatingSystem = gwmi Win32_OperatingSystem 
write-host $Win32_OperatingSystem.MUILanguages 
fr-FR en-US it-IT

Display Windows defender status
1
2
3
4
5
6
7
8
9
$Test_Win_Defender = Get-Service -DisplayName 'Windows Defender'
If ($Test_Win_Defender.Status -eq "Stopped")
 {
  write-host "Disbaled" -foregroundcolor "yellow"
 }
Else
 {
  write-host "Enabled" -foregroundcolor "green" 
 } 

Display Firewall status
1
2
3
4
5
6
7
8
9
$Firewall_state = $REG_Firewall.EnableFirewall
If ($Firewall_state -eq "0")
 {
  write-host "Disbaled" -foregroundcolor "yellow"
 }
Else
 {
  write-host "Enabled" -foregroundcolor "green" 
 }
Display installed RAM
1
2
3
4
$Win32_ComputerSystem = gwmi Win32_ComputerSystem 
$Memory_RAM = [Math]::Round(($Win32_ComputerSystem.TotalPhysicalMemory/ 1GB),1) 
write-host $Memory_RAM + "GB"
3,3 Gb

List Hard drive
1
2
3
4
5
6
7
8
9
10
$Win32_LogicalDisk = get-wmiobject Win32_LogicalDisk | where {$_.DriveType -eq "3"}
#--------------- Disk informations : deviceid, totalsize; freespace #---------------
ForEach ($disk in $Win32_LogicalDisk) ### Enum Disk 
 {
    $Total_size = [Math]::Round(($disk.size/1GB),1)
    $Free_size = [Math]::Round(($disk.Freespace/1GB),1) 
    $Disk_information =  $Disk_information + "(" + $disk.deviceid + ") " + $Total_size + " GB Total / " +  + $Free_size + " GB Free `n"
 }
$Disk_information
(C:) 465.8 GB Total / 134.3 GB Free

Display the current Timezone
1
2
3
$Win32_TimeZone = gwmi Win32_TimeZone 
write-host $Win32_TimeZone.Caption 
(UTC+01:00) Brussels, Copenhagen, Madrid, Paris

Display Internet Explorer version
1
2
3
4
$REG_IE = gp -path registry::"HKLM\SOFTWARE\Microsoft\Internet Explorer"
$IE_Ver= $REG_IE.svcUpdateVersion + " (" + $REG_IE.svcKBNumber + ")"
write-host $IE_Ver
10.0.25 (KB3032359)
Display the SCCM site code
1
2
3
$REG_SCCM = get-itemproperty -path registry::"HKLM\SOFTWARE\Microsoft\SMS\Mobile Client"
write-host $REG_SCCM.AssignedSiteCode
SD1