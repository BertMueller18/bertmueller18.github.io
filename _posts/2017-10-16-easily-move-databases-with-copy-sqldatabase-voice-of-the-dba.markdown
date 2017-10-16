---
layout: post 
title:  "Easily Move Databases with Copy-SqlDatabase | Voice of the DBA" 
date:   2017-10-16T21:44:57.546Z 
categories: powershell sqlserver
link: https://voiceofthedba.com/2016/12/09/easily-move-databases-with-copy-sqldatabase/ 
tags:
  - links
ogtype: article 
---

> Easily Move Databases with Copy-SqlDatabase
Posted on December 9, 2016 by way0utwest
One of the things that people have asked to be implemented for many years is an easy way to copy databases. SSIS has the Copy Database Task, but that has been problematic over time. As a result, while easy, it’s cumbersome to take a backup of a database, copy it to a new instance, and restore it. Or use the detach/copy/attach/attach method.

dbatools gives us a nice, easy Posh command to perform this task: Copy-SqlDatabase. I made a quick test recently to see how this works. Using the –Whatif option, I tried to copy a database from one instance to another on my main computer.