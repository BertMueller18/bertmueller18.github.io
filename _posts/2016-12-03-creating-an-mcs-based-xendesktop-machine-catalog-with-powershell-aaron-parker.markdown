---
layout: post 
title:  "Creating an MCS-based XenDesktop Machine Catalog with PowerShell - Aaron Parker" 
date:   2016-12-03T11:50:59.369Z 
categories: citrix mcs xendesktop powershell
link: http://stealthpuppy.com/xendesktop-mcs-machine-catalog-powershell/ 
tags:
  - links
ogtype: article 
---

> Creating an MCS-based XenDesktop Machine Catalog with PowerShell

Driving XenDesktop with PowerShell is a challenge to say the least. While documentation for the XenDesktop PowerShell modules is OK and Citrix Studio outputs PowerShell code after you’ve completed a task in the console, there’s still plenty of work to get that code into something usable.

As part of an ongoing series of articles themed around automating virtual desktop deployment, I’ve written some PowerShell code to automate the creation of an non-persistent, MCS-based Machine Catalog based on a specific Windows image, that we’ve already automated with a solution such as MDT.

Don’t expect to copy and paste the PowerShell output in Citrix Studio and have a complete script. The code is missing a number of lines that link tasks together. I found this article on the Citrix Blogs quite useful – Using PowerShell to Create a Catalog of Machine Creations Services Machines; however I’ve taken my script a few steps further.