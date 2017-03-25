---
layout: post 
title:  "AppV Powershell package creation - AppDetails" 
date:   2017-03-25T16:35:31.808Z 
categories: appv app-v powershell
link: http://www.appdetails.com/forums/topic/appv-powershell-package-creation/ 
tags:
  - links
ogtype: article 
---

> Good Afternoon,

A favorite trick of mine which i dont use nearly often enough is the use of powershell to create packages, this comes into its own when creating packages for applications which are regualrly updated such as Firefox.

Powershell Command:

#Configure Variables
$PName = Mozilla_Firefox_38.5.2_ESR_R01
$TPath = C:\Users\seq\Desktop\FireFox\FireFox_AppV5SequencerTemplate.appvt
$OPath = C:\Users\seq\Desktop\Mozilla_Firefox_38.5.2_ESR_R01
$PVAD = C:\Mozilla_Firefox_38.5.2_ESR_R01
$Source = C:\Users\seq\Desktop\FireFox
$Installer = C:\Users\seq\Desktop\FireFox\AppV_FireFox_Install.cmd

#Installation Script
Import-Module AppvSequencer
New-Item -Path $PVAD -ItemType Directory
CD $Source
New-AppvSequencerPackage -Name $PName -TemplateFilePath $TPath -OutputPath $OPath -PrimaryVirtualApplicationDirectory $PVAD -Installer $Installer -FullLoad

