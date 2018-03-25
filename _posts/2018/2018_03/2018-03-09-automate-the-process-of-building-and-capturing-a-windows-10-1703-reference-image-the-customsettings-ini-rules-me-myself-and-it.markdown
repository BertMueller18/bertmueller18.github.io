---
layout: post 
title:  "Automate the Process of Building and Capturing a Windows 10 1703 Reference Image: The CustomSettings.ini Rules | Me, Myself and IT" 
date:   2018-03-09T10:40:47.681Z 
categories: mdt mdt2013 reference deployment automation
link: https://emeneye.wordpress.com/2017/05/05/automate-the-process-of-building-and-capturing-a-windows-10-1703-reference-image-the-customsettings-ini-rules/ 
tags:
  - links
ogtype: article 
---

> Automate the Process of Building and Capturing a Windows 10 1703 Reference Image: The CustomSettings.ini Rules
May 5, 2017 Naz Windows DeploymentMDT, Microsoft Deployment Toolkit
We left the previous post in this series after having created our build and capture task sequence and having generated a boot image ISO.

As I explained in the post, to build and capture our reference image you will use the boot image ISO to fire up a virtual machine into the MDT Deployment Wizard where you go through a number of wizard panes. This is normally a manual process where you have to enter the keyboard language, region, time zone, etc and select the task sequence to run and whether you want to capture an image.

This post is all about eliminating this manual process with the help of the CustomSettings.ini rules which essentially providing answers to the wizard panes and thereby skipping this step altogether.