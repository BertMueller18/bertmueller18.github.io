---
layout: post 
title:  "Automate WSUS Using the PowerShell UpdateServices Module -- Microsoft Certified Professional Magazine Online" 
date:   2017-10-23T19:50:58.684Z 
categories: powershell wsus maintenance
link: https://mcpmag.com/articles/2017/08/10/automate-wsus-using-the-powershell-updateservices.aspx 
tags:
  - links
ogtype: article 
---

> Automate WSUS Using the PowerShell UpdateServices Module
By Boe Prox08/10/2017
Managing the WSUS has evolved over the course of the years from a Web page to using a MMC which still connects to the WSUS on either port 80 or 443 (as well as 8350 and 8351 as alternate ports).  Automating and managing the clients and updates through the MMC, while still a viable option, can be time consuming and doesn't allow for easy reporting of the state of the updates or clients.

Using PowerShell, we can automate update approvals, or decline updates which are not useful for our network like the Itanium updates. We can also generate reports which may not be as easy to do using the built-in reports on the WSUS console.

To begin working with WSUS, we need to import the UpdateServices module. Note that this module is available on Windows 2012 and above as well as Windows 8 and above. Once we have the module installed on the system, we can load the module via Import-Module.