---
layout: post 
title:  "Update Manually Installed PowerShell Modules from the PowerShell Gallery – Mike F Robbins" 
date:   2017-11-15T07:21:27.579Z 
categories: powershell  deployment oneget powershellgallery
link: http://mikefrobbins.com/2016/06/09/update-manually-installed-powershell-modules-from-the-powershell-gallery/ 
tags:
  - links
ogtype: article 
---

> Update Manually Installed PowerShell Modules from the PowerShell Gallery

MIKE F ROBBINS JUNE 9, 2016 0
There are PowerShell modules that ship with Windows 10 that weren’t installed from the PowerShell Gallery using PowerShellGet so they can’t be updated using the Update-Module cmdlet. This also applies for any modules that you’ve installed manually yourself.

The following PowerShell script retrieves a list of the most recent version of the modules in the all users path for PowerShell modules. It determines which ones weren’t installed using PowerShellGet based on the hidden xml file that would exist in the module directory and then it determines if a newer version exists in one of the PowerShell Galleries that’s registered on your computer: