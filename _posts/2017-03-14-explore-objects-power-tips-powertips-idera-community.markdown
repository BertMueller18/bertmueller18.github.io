---
layout: post 
title:  "Explore Objects - Power Tips - PowerTips - IDERA Community" 
date:   2017-03-14T22:02:21.379Z 
categories: powershell programming
link: http://community.idera.com/powershell/powertips/b/tips/posts/explore-objects 
tags:
  - links
ogtype: article 
---

> Explore Objects

In PowerShell, anything is represented by objects, and here is a helpful one-liner that examines any object and copies its members as text into your clipboard.

"Hello" | 
  Get-Member |
  Format-Table -AutoSize -Wrap |
  Out-String -Width 150 |
  clip.exe
Simply replace “Hello” with any variable or command, and see what is copied to your clipboard. You can then paste the information to the text editor or word processor of choice and print it or convert it to PDF for future reference.

