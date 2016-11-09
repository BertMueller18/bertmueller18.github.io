---
layout: post 
published: true 
title: "LabCenter News | Find VHDs that are not connected to a VM - PowerShell is King" 
date: 2016-11-09T19:19:54.155Z 
link: http://www.labcenternews.se/bloggers/mikael-nystroem/find-vhds-that-are-not-connected-to-a-vm-powershell-is-king/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Working with VM’s in Hyper-V means that you will eventually have VHD’s that are not connected, not not even in use. That happens when you remove the VM configuration from Hyper-V manager, but you told your self “I will remove the data files later”, later very rarely happens, at least not for my lab and my demo environment (in production we use SCVMM and this issues is much less). In many cases this consumes space and I can use that space for other purposes.