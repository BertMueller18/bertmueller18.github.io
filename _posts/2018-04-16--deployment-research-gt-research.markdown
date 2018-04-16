---
layout: post 
title:  "	Deployment Research &gt; Research" 
date:   2018-04-16T13:36:44.858Z 
categories: deployment intune powershell
link: https://deploymentresearch.com/Research/Post/663/Cloud-OS-Deployment-Part-1-Running-MDT-Task-Sequences-from-Microsoft-Intune 
tags:
  - links
ogtype: article 
---

## Cloud OS Deployment, Part 1 - Running MDT Task Sequences from Microsoft Intune
Deployment Research
Johan Arwidmark
Jan
23
2018
In this post you learn how to run MDT Task sequences, for either Computer refresh or Inplace-upgrades, from Microsoft Intune. Using task sequences gives you much better control of the Windows 10 servicing compared to regular features updates. And, as you probably figured out from the title already, there are more posts coming…:)

Credits goes to Peter Delch Dahl ( @PeterSelchDahl ) and Oliver Kieselbach ( @okieselb ) for excellent info on PowerShell script support in Intune.

Setup MDT for Microsoft Intune
Since Intune doesn’t support applications larger the 2 GB, you have to use a regular Azure blob storage to store the OS deployment content, and then call that content from your deployment (assignment) in Microsoft Intune. To run MDT task sequences via Microsoft Intune, you need the following

A MDT media item with a Windows 10 image, drivers, task sequences etc..
An Intune subscription.
A little bit of PowerShell.