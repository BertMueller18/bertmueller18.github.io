---
layout: post 
title:  "Tricky PowerShell Pipeline Tricks – Playing With WMI – Working Sysadmin" 
date:   2017-07-29T21:27:35.949Z 
categories: powershell automation wmi
link: http://www.workingsysadmin.com/tricky-powershell-pipeline-tricks-playing-with-wmi/ 
tags:
  - links
ogtype: article 
---
## Tricky PowerShell Pipeline Tricks – Playing With WMI
February 11, 2015PowerShell, PowerShell ISE, WMIpowershell, powershell ise, wmi
Here’s a quick task: Get the WMI object win32_bios for a computer. Using PowerShell, that’s really easy. You just run Get-WMIObject win32_bios. Now what if you wanted all the extended properties of the object (not just the five that it normally returns) and ONLY to return the properties that actually have a value assigned?

Well this question just got trickier. win32_bios isn’t very big so it’s an easy one to play with in this example. Let’s step through a couple commands so we know what we’re dealing with.


````powershell
Get-WMIObject win32_bios
 
 
SMBIOSBIOSVersion : 6.00
Manufacturer      : Phoenix Technologies LTD
Name              : PhoenixBIOS 4.0 Release 6.0     
SerialNumber      : VMware-42 00 a6 a6 02 95 ec 5e-89 05 0a cd b1 3b aa c6
Version           : INTEL  - 6040000
````
Well okay, there are the five properties that we knew the command returns by default. We know the extended properties are in there and we can prove it.

````powershell
Get-WMIObject win32_bios | Select-Object -Property *
 
 
PSComputerName        : workingsysadmin
Status                : OK
Name                  : PhoenixBIOS 4.0 Release 6.0     
Caption               : PhoenixBIOS 4.0 Release 6.0     
SMBIOSPresent         : True
__GENUS               : 2
__CLASS               : Win32_BIOS
__SUPERCLASS          : CIM_BIOSElement
__DYNASTY             : CIM_ManagedSystemElement
__RELPATH             : Win32_BIOS.Name="PhoenixBIOS 4.0 Release 6.0     ",SoftwareElementID="PhoenixBIOS 4.0 Release 6.0     ",SoftwareElementState=3,TargetOperatingSystem=0,Version="INTEL  - 6040000"
__PROPERTY_COUNT      : 27
__DERIVATION          : {CIM_BIOSElement, CIM_SoftwareElement, CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER              : workingsysadmin
__NAMESPACE           : root\cimv2
__PATH                : \\workingsysadmin\root\cimv2:Win32_BIOS.Name="PhoenixBIOS 4.0 Release 6.0     ",SoftwareElementID="PhoenixBIOS 4.0 Release 6.0     ",SoftwareElementState=3,TargetOperatingSystem=0,Version="INTEL  - 6040000"
BiosCharacteristics   : {4, 7, 8, 9...}
BIOSVersion           : {INTEL  - 6040000, PhoenixBIOS 4.0 Release 6.0     }
BuildNumber           : 
CodeSet               : 
CurrentLanguage       : 
Description           : PhoenixBIOS 4.0 Release 6.0     
IdentificationCode    : 
InstallableLanguages  : 
InstallDate           : 
LanguageEdition       : 
ListOfLanguages       : 
Manufacturer          : Phoenix Technologies LTD
OtherTargetOS         : 
PrimaryBIOS           : True
ReleaseDate           : 20110921000000.000000+000
SerialNumber          : VMware-42 00 a6 a6 02 95 ec 5e-89 05 0a cd b1 3b aa c6
SMBIOSBIOSVersion     : 6.00
SMBIOSMajorVersion    : 2
SMBIOSMinorVersion    : 4
SoftwareElementID     : PhoenixBIOS 4.0 Release 6.0     
SoftwareElementState  : 3
TargetOperatingSystem : 0
Version               : INTEL  - 6040000
Scope                 : System.Management.ManagementScope
Path                  : \\workingsysadmin\root\cimv2:Win32_BIOS.Name="PhoenixBIOS 4.0 Release 6.0     ",SoftwareElementID="PhoenixBIOS 4.0 Release 6.0     ",SoftwareElementState=3,TargetOperatingSystem=0,Version="INTEL  - 6040000"
Options               : System.Management.ObjectGetOptions
ClassPath             : \\workingsysadmin\root\cimv2:Win32_BIOS
Properties            : {BiosCharacteristics, BIOSVersion, BuildNumber, Caption...}
SystemProperties      : {__GENUS, __CLASS, __SUPERCLASS, __DYNASTY...}
Qualifiers            : {dynamic, Locale, provider, UUID}
Site                  : 
Container             :
````