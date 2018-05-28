---
layout: post 
title:  "	www.deploymentshare.com | Windows 10 Upgrade with MDT–A Walkthrough" 
date:   2018-05-28T08:08:43.887Z 
categories: mdt deployment win10
link: http://www.deploymentshare.com/post/2015/10/31/Windows-10-Upgrade-with-MDT-A-Walkthrough 
tags:
  - links
ogtype: article 
---

## Windows 10 Upgrade with MDT–A Walkthrough
31. Oktober 2015  Jonathan  Microsoft Deployment Toolkit , Windows 10  Kommentare (6)
So I wanted to test an in-place upgrade for upgrading Windows 7 to Windows 10. 

Working in an education environment I know I have the following to contend with:

1. BIOS and not UEFI machines
2. Roaming Profiles and Redirected Documents implemented
3. Precious Teaching data to preserve

First, the test bed.  I create a Generation 1 (BIOS) virtual machine on an UpgradeTest VM.  I install some education apps, add the machine to the domain and add in some data to preserve