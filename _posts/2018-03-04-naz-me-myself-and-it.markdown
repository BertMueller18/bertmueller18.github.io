---
layout: post 
title:  "Naz | Me, Myself and IT" 
date:   2018-03-04T11:03:23.227Z 
categories: mdt win10 windows10
link: https://emeneye.wordpress.com/author/emeneye/ 
tags:
  - links
ogtype: article 
---

## January 2018 Cumulative Update for Windows 10 1703 is Not Installing in Task Sequence

January 24, 2018 Hands On Learning in the LabSCCM, Windows 10
I recently upgraded to SCCM 1710 and also updated MDT to v8450 and ADK to v1709. After the upgrade, I discovered Software Updates were broken in my Task Sequences. Specifically the Windows updates weren’t being installed (except for a Adobe Flash security update) whereas the Office 2016 updates were installing fine. At first I thought the update to 1710 had broken it but after a little digging I found that the January Cumulative update looks for the existence of the following registry item before installing the update:

HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\QualityCompat"

Value Name="cadca5fe-87d3-4b96-b7fb-a231484277cc"

Type="REG_DWORD”

Data="0x00000000”
So if the registry item is not present then the January cumulative update will not install as documented by Microsoft.