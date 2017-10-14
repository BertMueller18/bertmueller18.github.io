---
layout: post 
title:  "Windows 10 in-place upgrade with PowerShell and MDT – 4sysops" 
date:   2017-10-11T20:21:15.464Z 
categories: deployment windows10 usmt
link: https://4sysops.com/archives/windows-10-in-place-upgrade-with-powershell-and-mdt/ 
tags:
  - links
ogtype: article 
---

> Windows 10 in-place upgrade with PowerShell and MDT
Home  Blog  Windows 10 in-place upgrade with PowerShell and MDT4sysops - The online community for SysAdmins and DevOps
Dan Franciscus  Tue, Jun 20 2017  powershell, powershell scripts  2 
In this article, I will demonstrate how to use Microsoft Deployment Toolkit (MDT) and PowerShell to create a reusable in-place upgrade process for domain-joined computers.
AboutLatest Posts

Dan Franciscus
Dan Franciscus is a systems engineer and VMware Certified Professional (VCP) specializing in VMware, PowerShell, and other Microsoft-based technologies. You can reach Dan at his blog or his Twitter at @dan_franciscus.
Contents of this article
Setting up MDT
Overview of the Invoke-Win10Upgrade function
Stepping through Invoke-Win10Upgrade
Invoke-Win10Ugrade example
Code for Invoke-Win10Upgrade
This is a completely automated process. Thus, no end-user interaction is necessary, and it can take place on any remote computer. Although I have not tested it specifically, theoretically this function should be able to upgrade hundreds of workstations simultaneously with the proper computing in place.