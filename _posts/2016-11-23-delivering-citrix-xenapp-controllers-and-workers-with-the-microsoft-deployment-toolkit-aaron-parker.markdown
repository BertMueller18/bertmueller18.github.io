---
layout: post 
title:  "Delivering Citrix XenApp Controllers and Workers with the Microsoft Deployment Toolkit - Aaron Parker" 
date:   2016-11-22T23:07:17.367Z 
categories: citrix xenapp xendesktop pvs mdt mdt2013
link: http://stealthpuppy.com/delivering-citrix-xenapp-controllers-and-workers-with-the-microsoft-deployment-toolkit/ 
tags:
  - links
ogtype: article 
---

> Delivering Citrix XenApp Controllers and Workers with the Microsoft Deployment Toolkit

Here’s a quick a dirty method of controlling whether your Microsoft Deployment Toolkit (MDT) task sequence deploys a XenApp Controller (broker, XML service) or Worker (session host).

Let’s assume that you are automating the deployment of your XenApp image using MDT in an environment with XenApp Controllers and Workers. It makes sense to use the same task sequence to deploy both XenApp roles because there’s not a lot of difference between both server types (maybe on the Controllers we could avoid installing applications).