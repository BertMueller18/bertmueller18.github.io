---
layout: post 
title:  "DexterPOSH's Blog: PowerShell : Trust network share to load modules &amp; ps1" 
date:   2017-02-12T09:43:35.377Z 
categories: powershell deployment security
link: http://www.dexterposh.com/2017/01/powershell-trust-network-share-to-load.html 
tags:
  - links
ogtype: article 
---

> uesday, January 31, 2017
PowerShell : Trust network share to load modules & ps1
Problem

Do you have a central network share, where you store all the scripts or PowerShell modules ?
What happens if you try to run the script from a network share ? or if you have scripts (local) which invoke scripts or import PowerShell modules stored on this network share ?
