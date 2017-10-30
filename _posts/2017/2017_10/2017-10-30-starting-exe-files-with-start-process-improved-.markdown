---
layout: post 
title:  "Starting EXE Files with Start-Process (Improved)" 
date:   2017-10-30T12:02:02.669Z 
categories: powershell programming deployment
link: http://www.adamtheautomator.com/powershell-start-process-improved/ 
tags:
  - links
ogtype: article 
---

> STARTING EXE FILES WITH START-PROCESS (IMPROVED)
October 23, 2017	Leave a comment
PowerShell has many different ways to start a process. We’ve got Start-Process, Invoke-Expression, we can call the executable directly or use the ampersand (&) to invoke expressions. The most common way is to use Start-Process because it’s probably the most intuitive. PowerShell is known for it’s intuitive approach to command naming and Start-Process is an excellent choice. However, that command is limited.

To understand why Start-Process and all of these other commands are limited you first have to understand how a typical EXE file works. When an EXE file is run, it performs whatever action it was designed to do; it pings something (ping), starts a software installer (setup), looks up some DNS record (nslookup), whatever. For this part, Start-Proces and other commands to start a process work great. It’s simple. The limitation comes when that EXE returns some output.