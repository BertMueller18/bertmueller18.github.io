---
layout: post 
title:  "RD Gateway behind NetScaler | WTSLab's CEO Blog" 
date:   2016-12-06T12:58:09.180Z 
categories: netscaler rds networking
link: http://blog.wtslabs.com/?p=427 
tags:
  - links
ogtype: article 
---

> How-to: RD Gateway behind a NetScaler
This entry was posted in NetScaler Remote Desktop Services  on November 3, 2016 by crod
Before jumping in on how to get this done, let’s take a step back and review what the problem is and why this makes sense.

The Issue

If you are cheap and like to run your labs (or parts of it) at home, that probably means you have a single IP address available and exposed to the outside world and either no way to get a second one or no money for it. Basically you are like me.

That poses a problem when you want to have in your lab everything you can throw at it and still make sure it is all accessible from the outside, over that single IP address. That may include things like a fully functional RDS environment (with RD Web Access, RD Gateway, etc), a XenApp/XenDesktop one and even VMware Horizon. Problem is as soon as one is up, you will have to point your firewall to the internal resource that is doing whatever role (i.e. RD Gateway) and now port 443 is gone. Sure you could then start doing other services on different ports but that creates a mess. Not only not everything allows you to use different ports but having to open several ports to the outside creates a problem. This is the problem in a nutshell.