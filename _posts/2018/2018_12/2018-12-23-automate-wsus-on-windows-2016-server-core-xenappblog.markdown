---
layout: post 
title:  "Automate WSUS on Windows 2016 Server Core - xenappblog" 
date:   2018-12-23T10:38:01.414Z 
categories: wsus automation server2016
link: https://xenappblog.com/2017/automate-wsus-on-windows-2016-server-core/ 
tags:
  - links
ogtype: article 
---

> Automate WSUS on Windows 2016 Server Core
Tweet
61
Share
5
66 SHARES
Windows 2016 Server Core is a great choice for hosting your Windows Server Update Services (WSUS). In this post I’m going to show you how to install, configure and decline superseded updates which will save you losts of time and disk space.



First of all you’ll need to install Windows 2016 Core and configure it’s host name, IP address, join domain, time zone etc using sconfig.exe. I’ve automated all this in my Automation Framework and the following PowerShell script is used in a Task Sequence to automatically install and configure WSUS.