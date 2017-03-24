---
layout: post 
title:  "PowerShell Error Output – Mitch Klann's Blog – Mostly Automated" 
date:   2017-03-24T15:52:14.937Z 
categories: powershell programming
link: https://blogs.technet.microsoft.com/mitchk/2017/03/09/powershell-error-output/ 
tags:
  - links
ogtype: article 
---

> PowerShell Error Output
★★★★★★★★★★★★★★★
mitch-kMarch 9, 20170 
5
0
I’ve implemented some crazy ways of error handling over the years.  I wanted to quickly show and explain what I currently put in my Catch block for most of my PowerShell functions.  Here is a typical catch statement in one of my functions:
Write-Warning “Unexpected error occurred while executing $((Get-PSCallStack)[0].Command) with exception: $($_.Exception.Message)”

Write-Warning “Command: `’$($_.InvocationInfo.Line.Trim())`'”
I’ll usually have some error handling for specific conditions such as unexpected object state/data which usually results in a return from the function, so if we actually hit a catch block, something is REALLY not right.  If you have a script with several hundred lines, a dozen functions and you suddenly hit an unexpected error, it can be tedious to figure out where the error actually came from.  In the past, I’ve gone back to my scripts, added a bunch of ‘Write-Host “Just passed this section of code”’ or similar debug lines.  I very rarely have to perform this level of debugging with my current catch block reporting.