---
layout: post 
title:  "Installing and Configuring Microsoft Deployment Toolkit (MDT) 2013 on Windows Server 2012 R2" 
date:   2017-09-24T12:29:04.095Z 
categories: mdt deployment powershell mdt2013 win10
link: http://blog.itvce.com/2013/10/27/installing-and-configuring-microsoft-deployment-toolkit-mdt-2013-on-windows-server-2012-r2/ 
tags:
  - links
ogtype: article 
---

> 
Posted OCT 27 2013 by DANE YOUNG with 22 COMMENTS


Last week I gave a presentation at the local Citrix Users Group in Santa Clara on Microsoft Deployment Toolkit (MDT) 2013 and Windows Server 2012 R2.  During the session, I had a 20 minute demo where I went through the basic installation and configuration of MDT 2013 on Windows Server 2012 R2. I enjoyed presenting the demo so much that I have decided to capture it into a blog post to help those new to the Microsoft Deployment Toolkit!  If you want a quick overview and primer on MDT, go check out my presentation and previous blog post here: Bay Area Citrix Users Group October 23rd Presentation – Microsoft Deployment Toolkit (MDT) 2013 Primer!

In this post we are going to be covering slides 10-14 from my presentation, the live installation and configuration demo. Let’s get started!  For this demo, I will be using two systems, the first is my MDT 2013 server, running Windows Server 2012 R2. The second is my MDT client/target, to which I will be deploying Windows Server 2012 R2 from a volume license ISO. On the MDT server, I will start by downloading the Microsoft Assessment and Deployment Kit (ADK) for Windows 8.1 which can be found here: http://www.microsoft.com/en-us/download/details.aspx?id=39982.

