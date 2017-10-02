---
layout: post 
title:  "Journey into Windows 10 in-place upgrade troubleshooting hell - WinSysBlog" 
date:   2017-10-02T09:50:03.596Z 
categories: windows10 migration MDT MDT2013
link: https://winsysblog.com/2017/09/journey-windows-10-place-upgrade-troubleshooting-hell.html 
tags:
  - links
ogtype: article 
---

> Journey into Windows 10 in-place upgrade troubleshooting hell
Published by Dan Franciscus on September 8, 2017

Like many others organizations, mine is in the process of deploying Windows 10. Any new machine is now Windows 10, and we are now taking requests for users who want to do an in-place upgrade from 7 to 10. We are a small organization in comparison to most, so considering we do not use SCCM due to the cost, we needed to use another tool to do an in-place upgrade. For this reason, I created a PowerShell function that could perform multiple, remote, in-place upgrades to our AD-joined workstations using MDT. It does a great job, in fact I wrote an article about it, so if you are inclined to use it, grab it on Github.