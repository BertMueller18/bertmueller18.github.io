---
layout: post 
title:  "Auto-Logging Command Output - Power Tips - PowerTips - IDERA Community" 
date:   2017-08-02T21:01:56.056Z 
categories: powershell programming
link: http://community.idera.com/powershell/powertips/b/tips/posts/auto-logging-command-output 
tags:
  - links
ogtype: article 
---

> Auto-Logging Command Output

In the previous tip we introduced the PreCommandLookupAction supported by PowerShell 3 and better. Today we have a special implementation for you.

When you run below code, PowerShell will accept any command that starts with “*” and log the command output in a text file. The text file opens after the command is done.

So you can now run *dir instead of dir to log the results, or *Get-Process instead of Get-Process.

