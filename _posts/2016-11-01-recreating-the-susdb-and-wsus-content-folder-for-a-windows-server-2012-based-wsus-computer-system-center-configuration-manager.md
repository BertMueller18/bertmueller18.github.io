---
layout: post 
published: true 
title: "Recreating the SUSDB and WSUS Content folder for a Windows Server 2012 based WSUS computer | System Center: Configuration Manager" 
date: 2016-11-01T15:35:10.258Z 
link: https://blogs.technet.microsoft.com/configurationmgr/2016/10/18/recreating-the-susdb-and-wsus-content-folder-for-a-windows-server-2012-based-wsus-computer/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> System Center: Configuration Manager
Recreating the SUSDB and WSUS Content folder for a Windows Server 2012 based WSUS computer
★★★★★★★★★★★★★★★
October 18, 2016 by J.C. Hornbeck [MSFT] // 0 Comments

31
0
Author: Meghan Stewart | Support Escalation Engineer

Occasionally you may find that you want to start over in WSUS with a fresh database (SUSDB). There can be any number of reasons for this, but typically I see people doing this if their SUSDB is rather old, has a ton of unneeded updates in it, and maintenance has not been done on the SUSDB in years. In those cases you can find that a rebuild may be faster and easier than fixing the problematic SUSDB. Typically speaking, I see people wanting to recreate the just the content dir if they accidentally unchecked the “download update files to this server only when updates are approved” and ended up with a hard drive full of unneeded files. Whatever the reason, here are the steps for recreating the SUSDB and the WSUS Content folder for a Windows Server 2012 based WSUS computer: