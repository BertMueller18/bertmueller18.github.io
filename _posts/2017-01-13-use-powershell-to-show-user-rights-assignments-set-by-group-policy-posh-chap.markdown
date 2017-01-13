---
layout: post 
title:  "Use PowerShell to Show User Rights Assignments Set by Group Policy – PoSh Chap" 
date:   2017-01-13T15:09:55.650Z 
categories: powershell gpo
link: https://blogs.technet.microsoft.com/poshchap/2017/01/13/use-powershell-to-show-user-rights-assignments-set-by-group-policy/?utm_source=dlvr.it&utm_medium=twitter 
tags:
  - links
ogtype: article 
---

## Use PowerShell to Show User Rights Assignments Set by Group Policy

Here’s one I came across whilst performing some Group Policy troubleshooting…

 


Get-CimInstance -Query "Select * from RSOP_UserPrivilegeRight where precedence=1" -Namespace root\rsop\computer | 
Select-Object UserRight,AccountList

 