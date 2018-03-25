---
layout: post 
title:  "Viewing Your Drive Information with PowerShell -- Microsoft Certified Professional Magazine Online" 
date:   2018-03-25T15:45:27.558Z 
categories: powershell wmi reporting automation
link: https://mcpmag.com/articles/2018/01/26/view-drive-information-with-powershell.aspx 
tags:
  - links
ogtype: article 
---

> Viewing Your Drive Information with PowerShell
Using Windows Management Instrumentation makes it easy to pull information about the drives on your system or remote systems. Here's how.

By Boe Prox01/26/2018
Managing drives is a very common thing that a system administrator can do. Whether it is monitoring space to ensure that a drive doesn't run out of available capacity, to understanding just how many drives are on a single system, using PowerShell to provide information for this is something that every single system administrator who works with Windows should know!

Windows Management Instrumentation (WMI) can be a wealth of information that anyone should be able to query to locate pretty much whatever they need information on. In our search for information on all of the drives on our system, one of the more common WMI classes to query is the Win32_LogicalDisk class. This class contains information about all of the attached and mapped drives on a system. More information on this class can be found here.

We can run the following query using the Get-WMIObject cmdlet to find out more information about all of the drives on my system: