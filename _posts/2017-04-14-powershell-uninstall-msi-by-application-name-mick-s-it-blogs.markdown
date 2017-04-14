---
layout: post 
title:  "PowerShell: Uninstall MSI by Application Name | Mick's IT Blogs" 
date:   2017-04-14T19:41:55.953Z 
categories: deployment mdt powershell msi
link: https://mickitblog.blogspot.de/2017/03/powershell-uninstall-msi-by-application.html 
tags:
  - links
ogtype: article 
---

> PowerShell: Uninstall MSI by Application Name POSTED BY: MICK PLETCHER - 3:14 PM
SHARE& COMMENT  















Here is a function that will uninstall an MSI installed application by the name of the app. You do not need to input the entire name either. For instance, say you are uninstalling all previous versions of Adobe Reader. Adobe Reader is always labeled Adobe Reader X, Adobe Reader XI, and so forth. This script allows you to do this without having to find out every version that is installed throughout a network and then enter an uninstaller line for each version. You just need to enter Adobe Reader as the application name and the desired switches. It will then search the name fields in the 32 and 64 bit uninstall registry keys to find the associated GUID. Finally, it will execute an msiexec.exe /x {GUID} to uninstall that version.