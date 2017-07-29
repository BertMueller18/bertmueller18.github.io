---
layout: post 
title:  "Cyber Wardog Lab: Enabling Enhanced PowerShell logging &amp; Shipping Logs to an ELK Stack for Threat Hunting" 
date:   2017-07-29T21:29:19.304Z 
categories: powershell security
link: https://cyberwardog.blogspot.de/2017/06/enabling-enhanced-ps-logging-shipping.html?m=1 
tags:
  - links
ogtype: article 
---

## Enabling Enhanced PowerShell logging & Shipping Logs to an ELK Stack for Threat Hunting


A couple of weeks ago, I was asked how useful enabling enhanced PowerShell logging is for a Threat Hunter and how easy it is to ship its logs to an ELK stack for analysis. First, when I say enhanced PowerShell logging, I mean enabling Module & Script Block Logging. Those two enhancements started with Windows Management Framework (WMF) version 4.0 and 5.0 and are very useful to log PowerShell pipeline execution details and all blocks of PowerShell code as they get executed (Helpful against encoded and obfuscated scripts). Several experts have already explained the benefits of those enhancements in more details, but only a few have shown detailed steps for the implementation, consumption and analysis of the logs.

In this post, I will show you how you can enable enhanced PowerShell logging in your lab environment, create a Logstash Filter for it, and integrate it with other logs to improve your endpoint visibility while hunting for adversaries leveraging PowerShell (not just powershell.exe) during post-exploitation. 



### Requirements:
Sysmon Installed (I have version 6.X installed)
Winlogbeat forwarding logs to an ELK Server
I recommend to read my series "Setting up a Pentesting.. I mean, a Threat Hunting Lab" to help you set up your environment if you haven't set up one yet.
Windows Management Framework (WMF) 5.0 (Download)
PowerShell 5.0
I recommend to read about Logstash Filter Plugins specifically KV, GROK & MUTATE
PowerShell Empire 2.0 (Github)
