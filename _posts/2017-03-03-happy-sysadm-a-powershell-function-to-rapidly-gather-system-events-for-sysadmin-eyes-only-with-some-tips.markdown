---
layout: post 
title:  "Happy SysAdm: A PowerShell function to rapidly gather system events for sysadmin eyes only with some tips" 
date:   2017-03-03T06:40:38.494Z 
categories: powershell programming eventlog
link: http://www.happysysadm.com/2017/03/a-powershell-function-to-rapidly-gather.html 
tags:
  - links
ogtype: article 
---

A PowerShell function to rapidly gather system events for sysadmin eyes only with some tips
I suppose that we, sysadmins, have all been through that moment when an application developer bursts in behind your back just to tell you that his perfectly-coded application is getting stuck and he goes on stating that for sure something has happened at system level and you should already be checking.

This is the moment when being good at PowerShell comes to the rescue. Because with PowerShell you can quickly write a tool that allows you to check your event logs and extract just the right kind of information to show that the system has no issues (as it's often the case) and that he better be reviewing his software configuration.

PowerShell basically is your Splunk, but without the price tag