---
layout: post 
title:  "Posh-Sysmon Module for Creating Sysmon Configuration Files" 
date:   2017-09-30T09:08:22.969Z 
categories: powershell sysmon
link: https://www.darkoperator.com/blog/2017/2/17/posh-sysmon-powershell-module-for-creating-sysmon-configuration-files 
tags:
  - links
ogtype: article 
---

> SHELL IS ONLY THE BEGINNING
When getting shell is only the start of the journey.

BLOG  INFOSEC TACTICO PODCAST  SEARCH  BLOG SERIES  MSF INSTALLATION GUIDES  PROJECTS  ABOUT ME
Posh-Sysmon Module for Creating Sysmon Configuration Files

FEBRUARY 20, 2017 BY CARLOS PEREZ IN BLUE TEAM, POWERSHELL
Why a PowerShell Module

Sysmon configuration can be complex in addition to hard to maintain by hand. For this purpose I created a module called Posh-Sysmon some time ago to aid in the creation and maintenance of configuration files. The module was initially written after the release of version 2.0 and has been maintained and expanded as new version have been released all the way to the current one at the time of this blog post being written with version 6.0. 

The module is written for PowerShell v3.0 and above and can be installed from the PowerShell Gallery if running version 5.0 or 5.1 using the cmdlet 