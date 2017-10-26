---
layout: post 
title:  "Save yourself hours of time with this PowerShell PSReadline tweak - WinSysBlog" 
date:   2017-10-19T16:29:56.123Z 
categories: powershell programming
link: https://winsysblog.com/2017/10/save-hours-time-psreadline-tweak.html 
tags:
  - links
ogtype: article 
---

### Save yourself hours of time with this PowerShell PSReadline tweak
Published by Dan Franciscus on October 18, 2017

As someone who is absolutely obsessed with automation, I am always looking for little hacks or tweaks to make myself more efficient. Since I spend a lot of time in the PowerShell console, I thought I would share my favorite PSReadline setting and one that I HIGHLY recommend to anyone who wants to save themselves hours if not days of their life trying to remember exactly what command they used last week to do task X. With that said, I am not crazy about throwing in a lot of stuff into my profile, but for me this is a must have.

In my PowerShell profile I have two lines that modify my console experience:
````
Set-PSReadlineKeyHandler -Key UpArrow -Function HistorySearchBackward
Set-PSReadlineKeyHandler -Key DownArrow -Function HistorySearchForward````
So what do these two little beauties do exactly? They create and destroy worlds. Just kidding. They do save human lives though. Just kidding again. OK, enough with the suspense…