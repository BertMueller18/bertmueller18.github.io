---
layout: post 
title:  "Automated Driver Import in MDT 2013 | J. Gregs Brain Corral" 
date:   2017-10-24T06:39:04.098Z 
categories: deployment  driver mdt powershell
link: https://blog.uvm.edu/jgm/2013/11/06/automated-driver-import-in-mdt-2013/ 
tags:
  - links
ogtype: article 
---

> Automated Driver Import in MDT 2013
As a follow up to my previous post, I also have developed a script to automate the import of drivers into MDT 2013.  This PowerShell script takes a source folder structure and duplicates the top two levels of folders in the MDT Deployment Share “Out-of-box drivers ” branch.  The script then imports all drivers found in the source directories to the matching folders in MDT.

All we have to do is extract all drivers for a given computer model into an appropriately named folder in the source directory, and then run the script.