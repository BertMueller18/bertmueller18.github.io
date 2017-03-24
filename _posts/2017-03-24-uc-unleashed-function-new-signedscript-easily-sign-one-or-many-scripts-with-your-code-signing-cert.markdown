---
layout: post 
title:  "UC Unleashed » Function: New-SignedScript – Easily Sign One or Many Scripts with Your Code Signing Cert" 
date:   2017-03-24T15:54:33.840Z 
categories: powershell programming
link: https://www.ucunleashed.com/1496 
tags:
  - links
ogtype: article 
---

> Function: New-SignedScript – Easily Sign One or Many Scripts with Your Code Signing Cert
September 20th, 2012Pat RichardLeave a commentGo to comments
Signs a PowerShell script with a code signing certificate.

Syntax
New-SignedScript [[-path] ] [-Verbose] [-Debug] [-ErrorAction ] [-WarningAction ] [-ErrorVariable ] [-WarningVariable ] [-OutVariable ] [-OutBuffer ] [-WhatIf] [-Confirm]
Detailed Description
One of the concerns about using a PowerShell script is that it often requires the user to change the Execution Policy on the machine the script is running on. This can cause security concerns, because when the Execution Policy is lowered, any script can run, including those with malicious intent. For more information on setting the Execution Policy, see Set-ExecutionPolicy.