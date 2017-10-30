---
layout: post 
title:  "A great way to collect logs for troubleshooting | Virtualization Blog" 
date:   2017-10-30T17:06:09.860Z 
categories: powershell eventlog hyperv
link: https://blogs.technet.microsoft.com/virtualization/2017/10/27/a-great-way-to-collect-logs-for-troubleshooting/ 
tags:
  - links
ogtype: article 
---

## A great way to collect logs for troubleshooting

October 27, 2017 by Lars Iwer [MSFT] // 1 Comments

0
0
Did you ever have to troubleshoot issues within a Hyper-V cluster or standalone environment and found yourself switching between different event logs? Or did you repro something just to find out not all of the important Windows event channels had been activated?

To make it easier to collect the right set of event logs into a single evtx file to help with troubleshooting we have published a HyperVLogs PowerShell module on GitHub.

In this blog post I am sharing with you how to get the module and how to gather event logs using the functions provided.