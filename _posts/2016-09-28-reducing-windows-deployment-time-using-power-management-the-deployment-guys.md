---
layout: post 
published: true 
title: "Reducing Windows Deployment time using Power Management – The Deployment Guys" 
date: 2016-09-27T22:54:07.970Z 
categories: mdt deployment 
link: https://blogs.technet.microsoft.com/deploymentguys/2015/03/26/reducing-windows-deployment-time-using-power-management/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Reducing Windows Deployment time using Power Management
The following post was contributed by Benjamin Rampe a Senior PFE working for Microsoft.

While studying up on Windows 10, I came across a technique that has been shown to reduce the time it takes to apply an OS WIM to disk by 20 – 50%*.  That’s a fairly significant savings in time and the implementation of this technique is relatively easy and does not require you to change how you deploy Windows.  Believe it or not, the savings come from adjusting the OS power management settings during a deployment.  While there are multiple ways to implement these power management settings, below I’ve outlined what I consider the most non-intrusive to existing deployment methods. 