---
layout: post 
title:  "Pro Tip: PowerShell DSC Events to Monitor – GoateePFE" 
date:   2017-01-13T13:56:00.564Z 
categories: powershell psdsc
link: https://blogs.technet.microsoft.com/ashleymcglone/2017/01/12/pro-tip-powershell-dsc-events-to-monitor/ 
tags:
  - links
ogtype: article 
---

> Pro Tip: PowerShell DSC Events to Monitor
★★★★★★★★★★★★★★★
Ashley McGloneJanuary 12, 20170 
13
0
 The Problem
I need to monitor PowerShell DSC health on all of my nodes. But I do not want to wait for every possible event to happen in production to catch it and add it to my monitoring event list.

The Options
There are many options for monitoring PowerShell Desired State Configuration (DSC) status on your Windows nodes:

DSC reporting server
Get-DSCConfigurationStatus / Test-DSCConfiguration
xDscDiagnostics
OMS / Azure Automation DSC
Harvest and parse the status files under C:\Windows\System32\Configuration\ConfigurationStatus\
Event logs (which logs and events to capture?)
Windows Event Forwarding
Enterprise tools: Splunk, Nagios, SCOM, etc.