---
layout: post
published: true
title: "PowerShell DSC Resource for Managing Repositories and Modules | Tao Yang's System Center Blog"
date: 2016-09-15T13:08:49.910Z
categories: powershell psdsc  
link: http://blog.tyang.org/2016/09/15/powershell-dsc-resource-for-managing-repositories-and-modules/
tags:
  - links
ogtype: article
bodyclass: post
---

> PowerShell DSC Resource for Managing Repositories and Modules
Posted on Sep 15, 2016Written by Tao Yang
0
Introduction
PowerShell version 5 has introduced a new feature that allows you to install packages (such as PowerShell modules) from NuGet repositories. If you have used cmdlets such as Find-Module, Install-Module or Uninstall-Module, then you have already taken advantage of this awesome feature.

By default, a Microsoft owned public repository PowerShell Gallery is configured on all computers running PowerShell version 5 and when you use Find-Module or Install-Module, you are pulling the modules from the PowerShell Gallery.

Ever since I started using PowerShell v5, I’ve discovered some challenges managing modules for machines in my environment:

Lack of a fully automated way to push modules to a group of computers
Module version inconsistency between computers
Need of a private repository
Let me elaborate each of the point listed above.
