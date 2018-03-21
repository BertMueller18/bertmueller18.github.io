---
layout: post 
title:  "Invoke-PnPReScan | Fredrik Wall" 
date:   2018-03-21T23:19:10.016Z 
categories: deployment powershell automation
link: http://fredrikwall.se/powershell/invoke-pnprescan/ 
tags:
  - links
ogtype: article 
---

> Invoke-PnPReScan
BY FREDRIK · JANUARY 30, 2018

When working with client management and deployment you some times need to do a plug n play rescan when installing drivers.
Using device manager and right click and click on Scan for Hardware changes is not an alternetive then.

Using Microsofts Devcon.exe file with Rescan is an alternetive.
But then you need to distribute that file to your clients and run it.

When we did the PowerShell GeekEnd with the PowerShell User Group Sweden in November this was a question that was up
when we started to talk about creating cool stuff with PowerShell.

We ended up finding a PowerShell solution that was written as an example for using C# code with PowerShell.
And in my solution “Invoke-PnPReScan.ps1” I use that plus a solution for start PowerShell as administrator.
Because this script need to be running as administrator or else nothing will happen.