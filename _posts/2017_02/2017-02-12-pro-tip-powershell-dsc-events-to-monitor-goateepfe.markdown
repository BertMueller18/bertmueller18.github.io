---
layout: post 
title:  "Pro Tip: PowerShell DSC Events to Monitor – GoateePFE" 
date:   2017-02-12T09:37:26.138Z 
categories: psdsc programming deployment
link: https://blogs.technet.microsoft.com/ashleymcglone/2017/01/12/pro-tip-powershell-dsc-events-to-monitor/ 
tags:
  - links
ogtype: article 
---

> The Problem
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
I am not saying any one of these options is better than the other. Some would certainly require more work.

One of the easiest options is to simply monitor the Windows event log on your DSC nodes. (While DSC is now available on other platforms, this tip is for Windows nodes.)