---
layout: post 
title:  "The Startup Script is Dead | Ask  Premier Field Engineering (PFE)  Platforms" 
date:   2017-08-25T19:07:54.921Z 
categories: powershell automation deployment
link: https://blogs.technet.microsoft.com/askpfeplat/2015/04/26/the-startup-script-is-dead/ 
tags:
  - links
ogtype: article 
---

> The Startup Script is Dead
★★★★★★★★★★★★★★★
April 26, 2015 by Mark Morowczynski [MSFT] // 17 Comments

0
0
Get ready to have an opinion!  Matthew Reynolds (https://twitter.com/MatthewMWR) here with my personal advice (not announcing any product changes) about which configuration vectors are working well and which are not—for today and tomorrow’s enterprises.

Any of these sound familiar?
· “I need to run <insert IT task> on every PC in the organization.”
· “Our startup scripts don’t run reliably”
· “People are complaining about slow logons”
We’ve all faced these scenarios right? In IT we need to run jobs on managed machines—whether to set a registry value, update files, fix a management agent or <insert automation challenge of the week>.

Boot & logon (particularly on client machines, but increasingly even for servers) have become an IT dead zone where automation and configuration vectors fall apart. Meanwhile people are stuck waiting for slow starting machines while traditional IT tasks (whether Foreground Group Policy, auto-start services, boot triggered scheduled tasks, etc.) time-out and fail in the background. No one wins.