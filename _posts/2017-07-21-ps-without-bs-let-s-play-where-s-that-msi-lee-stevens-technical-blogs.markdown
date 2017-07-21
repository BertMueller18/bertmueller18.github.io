---
layout: post 
title:  "PS without BS: Let’s play “Where’s that MSI?” – Lee Stevens: Technical Blogs" 
date:   2017-07-20T22:20:46.612Z 
categories: powershell msi deployment
link: https://blogs.technet.microsoft.com/leesteve/2017/07/19/ps-without-bs-lets-play-wheres-that-msi/ 
tags:
  - links
ogtype: article 
---

## PS without BS: Let's play "Where's that MSI?"
That infamous folder c:\windows\installer can take up a lot of space and resources, more importantly, it's cryptic when you see a bunch of numbered MSI and MSP files.

### What is this good for?

Well, my favorite reason is that on occasion you can find the MSI of a software package that may require a manual install. This may allow you to deploy it silently. Apart from that, you may be looking to clean up your disk.

I threw a script together to try making some sense of it all.
````powershell
$Files=gci -Path $env:windir\installer\*.msi
ForEach ($file in $files) {
try {
$WindowsInstaller = New-Object -ComObject WindowsInstaller.Installer
$MSIDatabase = $WindowsInstaller.GetType().InvokeMember("OpenDatabase","InvokeMethod",$Null,$WindowsInstaller,@($File.FullName,0))
$Query1 = "SELECT Value FROM Property WHERE Property = 'ProductName'"
$Query2 = "SELECT Value FROM Property WHERE Property = 'ProductVersion'"
$Query3 = "SELECT Value FROM Property WHERE Property = 'ProductCode'"
$View = $MSIDatabase.GetType().InvokeMember("OpenView","InvokeMethod",$null,$MSIDatabase,($Query1))
$View.GetType().InvokeMember("Execute", "InvokeMethod", $null, $View, $null)
$Record = $View.GetType().InvokeMember("Fetch","InvokeMethod",$null,$View,$null)
$Value = $Record.GetType().InvokeMember("StringData","GetProperty",$null,$Record,1)
$View = $MSIDatabase.GetType().InvokeMember("OpenView","InvokeMethod",$null,$MSIDatabase,($Query2))
$View.GetType().InvokeMember("Execute", "InvokeMethod", $null, $View, $null)
$Record = $View.GetType().InvokeMember("Fetch","InvokeMethod",$null,$View,$null)
$Value2 = $Record.GetType().InvokeMember("StringData","GetProperty",$null,$Record,1)
$View = $MSIDatabase.GetType().InvokeMember("OpenView","InvokeMethod",$null,$MSIDatabase,($Query3))
$View.GetType().InvokeMember("Execute", "InvokeMethod", $null, $View, $null)
$Record = $View.GetType().InvokeMember("Fetch","InvokeMethod",$null,$View,$null)
$Value3 = $Record.GetType().InvokeMember("StringData","GetProperty",$null,$Record,1)
write-host $file','$Value','$value2','$value3
}
catch {
Write-Output $_.Exception.Message
}
}
````
This script will give output that will explain the actual MSI file in CSV format. So, if you are looking for a reinstall, or even to install, this script should get you on your way. Here is the sample output.
````
C:\WINDOWS\installer\2b1add.msi,Microsoft Advanced Group Policy Management - Client,4.3.160.0,{2376566F-5F86-40BD-B51E-B0D7F02A5C77}
C:\WINDOWS\installer\3d71cb48.msi,Adobe Reader XI MUI,11.0.00,{AC76BA86-7AD7-FFFF-7B44-AB0000000001}
C:\WINDOWS\installer\409e40a.msi,Microsoft Visual C++ 2008 Redistributable - x86 9.0.30729.6161,9.0.30729.6161,{9BE518E6-ECC6-35A9-88E4-87755C07200F}
C:\WINDOWS\installer\42a77a14.msi,Orca,4.0.6001.0000,{4F34C602-4D6D-470D-A2A0-59E4F25DDBF2}
````