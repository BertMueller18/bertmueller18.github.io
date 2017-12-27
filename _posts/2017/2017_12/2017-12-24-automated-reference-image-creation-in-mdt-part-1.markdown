---
layout: post 
title:  "Automated Reference Image Creation in MDT - Part 1" 
date:   2017-12-24T10:14:19.877Z 
categories: mdt wsus automation imagefactory
link: https://trekker.net/archives/create-a-mostly-automated-reference-image-in-mdt-part-1/ 
tags:
  - links
ogtype: article 
---

> Create a [Mostly] Automated Reference Image in MDT – Part 1: Prerequisites
May 1, 2013Kyle Beckman

[Mostly] Automated Reference Image in MDT
Create a [Mostly] Automated Reference Image in MDT – Part 1: Prerequisites
Create a [Mostly] Automated Reference Image in MDT – Part 2: MDT Setup
Create a [Mostly] Automated Reference Image in MDT – Part 3: CustomSettings.ini and Bootstrap.ini
Create a [Mostly] Automated Reference Image in MDT – Part 4: Building the Image
Create a [Mostly] Automated Reference Image in MDT – Part 5: Pause/Suspend the Task Sequence
When it comes to deploying an operating system to a computer, speed and accuracy are the name of the game.  If you’re installing applications that are common across your organization as tasks in your OS deploy or installing the latest Windows updates after the deploy finishes, you can save tons of time by using a reference image.

So what is a reference image?  A reference image is a custom install of Windows that typically includes the latest Windows updates, common applications like Office, and any other customizations that are specific to computers in your environment that has been Sysprep’ed for redeployment to other computers.  Sounds easy so far, right?