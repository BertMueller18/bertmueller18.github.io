---
layout: post 
title:  "[Powershell] Citrix XenApp Monitoring Script ver. 2.1 | Pawel Serwan Blog" 
date:   2016-11-29T20:08:14.330Z 
categories: 
link: https://pawelserwan.wordpress.com/2015/03/26/powershell-citrix-xenapp-monitoring-script-ver-2-1/ 
tags:
  - links
ogtype: article 
---

> [Powershell] Citrix XenApp Monitoring Script ver. 2.1
26 March 2015 by pawelserwan	2 Comments

I got few questions regarding my Citrix XenApp monitoring script written in Powershell. I’ve decided to share with you it’s second better and improved version which has additional conditions on checking if really Citrix ICA connections was launched properly and your Citrix application is available for interaction with user. What is also improved is the overall time needed for the script to run. Right now all logons happen simultaneously thanks to which the script finishes below 2 minutes ( I tested that for about 20 servers). So you have now possibility to schedule a task that will be running more frequent and you will be able to better check health of your Citrix XenApp environment.