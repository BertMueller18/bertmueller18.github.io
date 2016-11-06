---
layout: post 
published: true 
title: "BGInfo for Windows 7 VMs running in Citrix PVS XenDesktop environments – JasonSamuel.com" 
date: 2016-09-08T08:31:44.206Z 
link: http://www.jasonsamuel.com/2012/12/27/bginfo-for-windows-7-vms-running-in-citrix-pvs-xendesktop-environments/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> CITRIX PROVISIONING SERVICESBGInfo for Windows 7 VMs running in Citrix PVS XenDesktop environmentsBy Jason Samuel
onDecember 27, 2012
1SHARESHARE TWEET SHARE SHARE 2 COMMENTS
If you’re running a Citrix VDI implementation using Provisioning Services (PVS) and XenDesktop, you need a way for your help desk and even the end user to easily identify the VM and pertinent system info easily. BGInfo is the tried and true way of doing this in a corporate environment. A simple overlay for the wallpaper. In a PVS environment, a lot of the info you would need to grab from a physical desktop are useless since it all goes away after the VM reboots and you’re back to a clean image. A lot of companies use BGInfo to quickly see troubleshooting data without having to use a management tool or agent. With PVS VMs, troubleshooting itself is rarely necessary. You just tell the user to reboot and they’re back to a clean slate. So BGInfo can be leveraged as more of an identification tool for when the user calls in than a troubleshooting tool. Download BGInfo from Microsoft here:

http://technet.microsoft.com/en-us/sysinternals/bb897557.aspx

I did a little custom BGInfo configuration to capture just the important pieces of info for my Windows 7 PVS XenDesktop environment. Of course this might differ for your environment and you might need more fields but this is a good starting point: