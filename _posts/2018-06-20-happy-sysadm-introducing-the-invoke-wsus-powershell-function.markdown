---
layout: post 
title:  "Happy SysAdm: Introducing the Invoke-Wsus PowerShell function" 
date:   2018-06-20T20:48:17.882Z 
categories: wsus powershell
link: http://www.happysysadm.com/2018/06/introducing-invoke-wsus-powershell.html?utm_source=feedburner&utm_medium=twitter&utm_campaign=Feed%3A+HappySysadm+%28Happy+SysAdm%29 
tags:
  - links
ogtype: article 
---

> Introducing the Invoke-Wsus PowerShell function
A couple of weeks ago I wrote a blog post on WSUS management with PowerShell. The post came with a script that could be used to manage automatic approvals of WSUS patches and updates.

This time I have decided to transform that script in an advanced PowerShell function named Invoke-WSUS (you can find it on my Github).

This function is kind of jack-of-all-trade: depending on the used parameter set, it can do a series of actions, as shown in the description and in the help file.