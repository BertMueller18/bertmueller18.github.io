---
layout: post 
published: true 
title: "Detecting Offensive PowerShell Attack Tools » Active Directory Security" 
date: 2016-08-01T07:06:16.457Z
categories: powershell pentest security
link: https://adsecurity.org/?p=2604 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Detecting Offensive PowerShell Attack Tools
ActiveDirectorySecurity, Malware, Microsoft Security, PowerShell, Technical Reference by Sean Metcalf
At DerbyCon V (2015), I presented on Active Directory Attack & Defense and part of this included how to detect & defend against PowerShell attacks.
Update: I presented at BSides Charm (Baltimore) on PowerShell attack & defense in April 2016.
The most important take-away from this post: you want to log all PowerShell activity and get that data into a central logging system to monitor for suspicious and anomalous activity.
The Evolution of PowerShell as an attack tool
PowerShell is a built-in command shell available on every supported version of Microsoft Windows (Windows 7 / Windows 2008 R2 and newer) and provides incredible flexibility and functionality to manage Windows systems. This power makes PowerShell an enticing tool for attackers. Once an attacker can get code to run on a computer, they often invoke PowerShell code since it can be run in memory where antivirus can’t see it. Attackers may also drop PowerShell script files (.ps1) to disk, but since PowerShell can download code from a website and run it in memory, that’s often not necessary.
Dave Kennedy & Josh Kelley presented at DEF CON 18 (2010) on how PowerShell could be leveraged by attackers. Matt Graeber developed PowerSploit and blogged at Exploit-Monday.com on why PowerShell is a great attack platform. Offensive PowerShell usage has been on the rise since the release of “PowerSploit” in 2012, though it wasn’t until Mimikatz was PowerShell-enabled (aka Invoke-Mimikatz) about a year later that PowerShell usage in attacks became more prevalent. PowerShell provides tremendous capability since it can run .Net code and execute dynamic code downloaded from another system (or the internet) and execute it in memory without ever touching disk. These features make PowerShell a preferred method for gaining and maintaining access to systems since they can move around using PowerShell without being seen. PowerShell Version 5 (v5) greatly improves the defensive posture of PowerShell and when run on a Windows 10 system, PowerShell attack capability is greatly reduced.