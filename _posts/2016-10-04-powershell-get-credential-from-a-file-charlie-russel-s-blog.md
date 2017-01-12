---
layout: post 
published: true 
title: "PowerShell: Get-Credential from a file | Charlie Russel's Blog" 
date: 2016-10-04T18:57:35.743Z
categories: powershell programming security 
link: http://blogs.msmvps.com/russel/2016/10/04/powershell-get-credential-from-a-file/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> PowerShell: Get-Credential from a file
Published 4 October, 2016
If you routinely have to log into a separate domain, it can be a nuisance to always have to run Get-Credential. Plus writing scripts with a -Credential parameter is a nuisance because if you call Get-Credential in the script, it will always prompt you.
 
I run a separate lab network here, with an Active Directory domain of TreyResearch.net. I got tired of always having scripts prompt me for credentials, or even more annoying, have routine PowerShell commands against computers in the lab fail because I didn't have credentials for that domain. The answer is pretty simple -- first, I stored my password securely in a file with: