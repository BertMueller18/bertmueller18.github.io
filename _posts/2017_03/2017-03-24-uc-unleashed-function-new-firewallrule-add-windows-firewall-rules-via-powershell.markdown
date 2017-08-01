---
layout: post 
title:  "UC Unleashed » Function: New-FirewallRule – Add Windows Firewall Rules Via PowerShell" 
date:   2017-03-24T15:48:32.906Z 
categories: powershellfirewall server2012 windows10
link: https://www.ucunleashed.com/1366 
tags:
  - links
ogtype: article 
---

> Function: New-FirewallRule – Add Windows Firewall Rules Via PowerShell
September 14th, 2012Pat RichardLeave a commentGo to comments
Description
Some of my scripts, namely Get-CsConnections.ps1, require specific firewall rules be created in order to operate correctly. So I set out to automate as much as possible the creation of these rules. A function was born.

This little function can do pretty much everything the Windows Firewall wizard can do. You can specify local and remote ports, local and remote IP addresses, programs, services, direction Inbound or Outbound), TCP/UDP or Any, and more. I borrowed some of the info from the Windows Firewall chm file for the comment-based help file in the function. Just run

Get-Help New-FirewallRule
for detailed help.

I tried to think of (and test) common requirements for firewall rules, but if I’ve left something out, or something isn’t working as expected, feel free to leave a comment below.