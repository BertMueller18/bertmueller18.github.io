---
layout: post 
title:  "Sysinternals Sysmon suspicious activity guide – Windows Security" 
date:   2018-10-23T10:32:47.667Z 
categories: sysmon microsoft activedirectory pentest security
link: https://blogs.technet.microsoft.com/motiba/2017/12/07/sysinternals-sysmon-suspicious-activity-guide/ 
tags:
  - links
ogtype: article 
---

## Sysinternals Sysmon suspicious activity guide

Sysmon tool from Sysinternals provides a comprehensive monitoring about activities in the operating system level. Sysmon is running in the background all the time, and is writing events to the event log.

You can find the Sysmon events under the Microsoft-Windows-Sysmon/Operational event log.

This guide will help you to investigate and appropriately handle these events.

Let's start with Microsoft Cybersecurity posture
 



Microsoft Cybersecurity posture consists of three pillars: Protect, Detect, and Respond. While Solid protection and rapid response capability are crucial, detection in depth is equally important. The focus in this blog post is on the last two:

Detect – Install and configure Sysmon to capture the relevant events
Respond - Investigate and respond to Sysmon events
