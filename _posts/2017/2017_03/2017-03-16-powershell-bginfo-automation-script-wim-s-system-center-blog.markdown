---
layout: post 
title:  "PowerShell: BgInfo Automation script | Wim's System Center blog" 
date:   2017-03-15T23:04:26.485Z 
categories: deployment mdt powershell 
tags:
  - links
ogtype: article 
---

PowerShell: BgInfo Automation script
February 23, 2017 at 9:19 am in BgInfo, Client Hyper-V, Hyper-V, PowerShell, scvmm, VM Template, Windows Server 2016, Windows Sysinternals, WS2016 by Wim Matthyssen

Probably everyone knows the Windows Sysinternals tool BgInfo (currently version 4.21). For those who don’t, it’s a great free tool which captures system information from a workstation or server (probably where it is the most useful) and displays the catched data on the Desktop of that machine. It can show useful information like, DNS settings, used IP Addresses, computer name, domain name, OS version, memory, etc. If you want to read more about this tool you can do so via following link: https://technet.microsoft.com/en-us/sysinternals/bginfo.aspx

Whenever I create a new Windows Server 2016 Virtual Machine (VM) template for customers, I mostly add this tool in the base image (also called golden image) and set it so it starts up automatically whenever a user logs on to the server. To automate this process, I wrote a PowerShell script which does all of the following:

Download the latest BgInfo tool
Create the BgInfo folder on the C drive
Extract and cleanup the BgInfo.zip file
Download the logon.bgi file which holds the preferred settings
Extract and cleanup the LogonBgi.zip file
Create the registry key (regkey) to AutoStart the BgInfo tool in combination with the logon.bgi config file
Start the tool for the first time