---
layout: post 
published: true 
title: "PowerShell Function to Create CimSessions to Remote Computers with Fallback to Dcom – Mike F Robbins" 
date: 2016-06-21T07:16:02.898Z
categories: powershell wmi cim
link: http://mikefrobbins.com/2014/08/28/powershell-function-to-create-cimsessions-to-remote-computers-with-fallback-to-dcom/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## PowerShell Function to Create CimSessions to Remote Computers with Fallback to Dcom

MIKE F ROBBINS AUGUST 28, 2014 1
I’ve found myself writing the same code over and over in my PowerShell scripts where I’m performing a task that requires me to create a CimSession to one or more computers without knowing what version of PowerShell is installed on the remote computers or if PowerShell is even installed on the remote computers.

While it is possible to create a CimSession to a remote computer in any of those scenarios I just described, it’s a fair amount of code to add to multiple scripts and then the same redundant code ends up being in multiple files which creates a nightmare if you ever find an issue with the code and need to update it for any reason.

I decided to turn the code I would use to create these CimSessions into a function which is shown below and add it to a script module so I could just call the function from the PowerShell script that needed the CimSessions created before the script performs its task(s).