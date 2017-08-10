---
layout: post 
title:  "Doing More with PowerShell Verbose Messages - Petri" 
date:   2017-03-01T19:20:13.597Z 
categories: powershell programming
link: https://www.petri.com/doing-more-with-powershell-verbose-messages 
tags:
  - links
ogtype: article 
---

## Doing More with PowerShell Verbose Messages


Whenever I teach about PowerShell scripting I always stress the value of using verbose messages in your functions and scripts. Assuming you are using cmdletbinding, and why wouldn’t you, you can insert Write-Verbose statements throughout your script. These statements won’t do anything unless your command is run with the common -Verbose parameter. However, these statements can be very useful for tracing and troubleshooting. I use these Verbose statements to help me track what my command is doing so that if it fails I have a better idea of where it failed and what it was doing. I don’t enjoy debugging and dealing with the interactive debugger and having Write-Verbose statements makes my life easier. Here are some ideas on how you might want to start using Write-Verbose.