---
layout: post 
title:  "Vacuum Breather - Managing MDT Out-of-the-Box Driver Repository using PowerShell" 
date:   2018-03-21T22:56:18.189Z 
categories: deployment mdt driver automation
link: http://vacuumbreather.com/index.php/blog/automation/item/29-managing-mdt-out-of-the-box-driver-repository-using-powershell 
tags:
  - links
ogtype: article 
---

## Managing MDT Out-of-the-Box Driver Repository using PowerShell
 Written by	Anton Romanyuk
Font Size      Print  Email Be the first to comment!
Rate this item1 2 3 4 5 (1 Vote)


In order to deploy Windows 10 with Microsoft Deployment Toolkit successfully, you need to keep drivers for the actual operating system up to date. In today’s blog I will discuss the approach that I use to import and update Out-Of-Box drivers in Microsoft Deployment Toolkit using PowerShell.

If you are used to designing deployment solutions for big customers, driver management sometimes becomes a very time consuming task. Additionally, in the time where everything happens so rapidly: we are now seeing Windows Insider Preview every other week, we have production releases of Windows 10 twice a year and every now and then there are new hardware models being adding to the lineup. The fast cadence of Windows feature updates means that you need to keep your driver repository up-to-date which can become a daunting and actually a pretty boring task. The good news is that you can simplify your Out-of-Box drivers management by leveraging Microsoft Deployment Toolkit's PowerShell module meaning you can import or update all of the drivers that will be needed into your MDT Deployment Workbench in a fingersnap.