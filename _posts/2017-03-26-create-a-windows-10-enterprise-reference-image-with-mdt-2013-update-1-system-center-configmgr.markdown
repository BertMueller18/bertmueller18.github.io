---
layout: post 
title:  "Create a Windows 10 Enterprise reference image with MDT 2013 Update 1 – System Center ConfigMgr" 
date:   2017-03-26T06:45:39.572Z 
categories: mdt deployment powershell win10
link: http://www.scconfigmgr.com/2015/10/24/create-a-windows-10-enterprise-reference-image-with-mdt-2013-update-1/ 
tags:
  - links
ogtype: article 
---

## Create a Windows 10 Enterprise reference image with MDT 2013 Update 1

Nickolaj AndersenOctober 24, 2015

16
This summer Microsoft released what they’re calling the last version of Windows, naming it Windows 10. Organizations that are looking into deploying Windows 10 will have to evaluate what scenario they will use, e.g. In-Place Upgrade, Provisioning or the traditional way of deploying an image. In this blog post, I will go through the steps required to setup a functional build server for reference images. The goal with this blog post is for you to get up and running with a functioning build server that will create the Windows 10 Enterprise reference image for bare metal deployments.