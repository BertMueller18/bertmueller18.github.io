---
layout: post 
title:  "Kevinisms: WSUS 2012 R2 Maintenance Automation" 
date:   2017-06-30T04:38:41.243Z 
categories: wsus powershell maintenance
link: http://kevinisms.fason.org/2017/06/wsus-2012-r2-maintenance-automation.html 
tags:
  - links
ogtype: article 
---
## Kevinisms: WSUS 2012 R2 Maintenance Automation

One of my most popular posts is WSUS automated maintenance, however it is centered on Server 2008 / 2008 R2. A friend asked me how I was doing it on Server 2012 R2 WSUS version 6.3 so I thought I would share that with the rest of the world. Server 2012 aka 6.2 should be no different.

I wont cover the reasons as they are explored in my above post as well as other places on the Internet, such as Jasons link below. This post is simply what I do to keep a 2012 R2 WSUS happy and fast. As before I perform 3 basic steps:
* Decline Itanium Updates
* Cleanup Wizard
* Re-Index Database