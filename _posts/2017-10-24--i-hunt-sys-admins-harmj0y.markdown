---
layout: post 
title:  "“I Hunt Sys Admins” – harmj0y" 
date:   2017-10-24T06:36:11.778Z 
categories: activedirectory security powershell pentest eventlog
link: http://www.harmj0y.net/blog/penetesting/i-hunt-sysadmins/ 
tags:
  - links
ogtype: article 
---

> “I Hunt Sys Admins”
Published January 19, 2015 by harmj0y
[Edit 8/13/15] – Here is how the old version 1.9 cmdlets in this post translate to PowerView 2.0:

Get-NetGroups  ->  Get-NetGroup
Get-UserProperties  ->  Get-UserProperty
Invoke-UserFieldSearch  ->  Find-UserField
Get-NetSessions  ->  Get-NetSession
Invoke-StealthUserHunter  ->  Invoke-UserHunter -Stealth
Invoke-UserProcessHunter  ->  Invoke-ProcessHunter -Username X
Get-NetProcesses  ->  Get-NetProcess
Get-UserLogonEvents  ->  Get-UserEvent
Invoke-UserEventHunter  ->  Invoke-EventHunter
[Note] This post is a companion to the Shmoocon ’15 Firetalks presentation I gave, also appropriately titled “I Hunt Sys Admins”. The slides are here and the video is up on Irongeek. Big thanks to Adrian, @grecs and all the other organizers, volunteers, and sponsors for putting on a cool event!