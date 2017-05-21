---
layout: post 
title:  "win10 unattend.xml settings | Support is &gt;Here&lt;" 
date:   2017-05-21T08:40:40.519Z 
categories: deployment win10 mdt2013
link: http://supportishere.com/2-unattend-xml-settings-i-specify-in-all-of-my-windows-10-installations/ 
tags:
  - links
ogtype: article 
---

> 2 Unattend.xml settings I specify in all of my Windows 10 installations.

By Brian Gonzalez | December 14, 2016 0 Comment
Share
  

There are others, but these are 2 I include in all of my Unattend.xml files.

Disable the First run animation from displaying:
reg add HKLM\Software\Microsoft\Windows\CurrentVersion\Policies\System /v EnableFirstLogonAnimation /t REG_DWORD /d 0 /f
Prevent the Network Selection box from appearing.
reg add HKLM\System\CurrentControlSet\Control\Network\NewNetworkWindowOff /F