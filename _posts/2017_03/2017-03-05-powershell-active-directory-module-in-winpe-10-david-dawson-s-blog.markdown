---
layout: post 
title:  "PowerShell Active Directory Module in WinPE 10 | David Dawson's blog" 
date:   2017-03-05T11:38:49.122Z 
categories: deployment winpe powershell
link: https://daviddawsonsblog.wordpress.com/2017/03/03/powershell-active-directory-module-in-winpe-10/ 
tags:
  - links
ogtype: article 
---

> POWERSHELL ACTIVE DIRECTORY MODULE IN WINPE 10
Posted on March 3, 2017 by daviddawsonsblog
When you are deploying an OS Task Sequence in Config Manager during the WinPE stage or using WinPE in general you may need to work with Active Directory using PowerShell for example to find an object or update a computer description. You could do this using ADSI but it would be much simpler if you could use the Active Directory module that is installed as part of the Remote Server Administration Tools.