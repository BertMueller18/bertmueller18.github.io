---
layout: post 
published: true 
title: "PowerShell and external commands done right // blog.edgylogic" 
date: 2016-09-27T22:52:14.715Z 
categories: powershell programming
link: http://edgylogic.com/blog/powershell-and-external-commands-done-right/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---
## PowerShell and external commands done right
Windows PowerShell is a massive step up from the VBScript horror used to manage Windows systems (I have no idea how people wrote websites with it without going mental). One of the things that annoyed me to no end though was how there seemed to be black magic involved when trying to make PowerShell execute external commands, i.e. not PowerShell cmdlets.

It is actually quite straight-forward once you wrap your head around it - it's just that we try to do things the way we did in VBScript or in OO languages, and PowerShell doesn't like that.