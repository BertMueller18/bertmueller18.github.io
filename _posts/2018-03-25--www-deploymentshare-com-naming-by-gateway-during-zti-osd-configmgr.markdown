---
layout: post 
title:  "	www.deploymentshare.com | Naming by Gateway during ZTI OSD–ConfigMgr" 
date:   2018-03-25T15:03:42.498Z 
categories: mdt deployment
link: http://www.deploymentshare.com/post/2017/02/01/Naming-by-Gateway-during-ZTI-OSD-ConfigMgr 
tags:
  - links
ogtype: article 
---

> Naming by Gateway during ZTI OSD–ConfigMgr
1. Februar 2017  Jonathan  Microsoft Deployment Toolkit , SCCM , System Center  Kommentare (0)
Hello internet!  Here I’m going to delve into the world of automatic computer naming by gateway using ConfigMgr.  Using a reference from Mikeal Nystrom (see links at the bottom of the page)  I’ve got this going with great effect in my environment so I though I’d share.

Firstly, before we go any further you are going to require MDT integration to get this to work.  We will create a MDT Settings package along the way as we create a task sequence and then configure the customsettings.ini to name the devices as we see fit.