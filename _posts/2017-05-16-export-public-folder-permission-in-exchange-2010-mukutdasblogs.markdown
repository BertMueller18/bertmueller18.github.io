---
layout: post 
title:  "Export Public Folder Permission in Exchange 2010 – MukutDasBlogs" 
date:   2017-05-16T05:09:07.507Z 
categories: exchange publicfolder powershell security
link: https://blogs.technet.microsoft.com/mukutdas/2014/06/27/export-public-folder-permission-in-exchange-2010/ 
tags:
  - links
ogtype: article 
---

## Export Public Folder Permission in Exchange 2010

I was asked how can we export Public Folder Permission including each nested folder to a CSV or TEXT File before restrict the users? And is there a way to re-assign the same permission to the particular Public Folder in the future?

 

This is very much achievable. Please follow below solution.  

 

Get-PublicFolderClientPermission:

Get-PublicFolder \ -Recurse | Get-PublicFolderClientPermission | Select-Object Identity,@{Expression={$_.User};Label="User";},@{Expression={$_.AccessRights};Label="AccessRights";} | Export-Csv C:\PublicFolderClientPermission.csv

 

 

Get-PublicFolderAdministrativePermission:

Get-PublicFolder \ -Recurse | Get-PublicFolderAdministrativePermission| Select-Object Identity,@{Expression={$_.User};Label="User";},@{Expression={$_.AccessRights};Label="AccessRights";},IsInherited,Deny | Export-Csv C:\PublicFolderAdministrativePermission.csv

 

 

