---
layout: post 
title:  "PowerShell remoting between two workgroup machines – Windows Management Infrastructure Blog" 
date:   2017-10-24T20:45:42.009Z 
categories: powershell remoting
link: https://blogs.msdn.microsoft.com/wmi/2009/07/24/powershell-remoting-between-two-workgroup-machines/ 
tags:
  - links
ogtype: article 
---

> PowerShell remoting between two workgroup machines
★★★★★★★★★★★★★★★
Nathan BurkhartJuly 24, 20090 
0
0
If you’re an IT Pro, PowerShell remoting is a great tool for doing quick, ad hoc management tasks on computers from the comfort of your own home or office.  However, before you can log into a machine, you have to make sure that it’s properly configured to grant you access – for safety’s sake, the default settings don’t allow remote access.  If the machine you’re trying to log into is in a Workgroup, which doesn’t have the same stringent security requirements and infrastructure of a typical Domain setting, you’ll have to modify a few additional settings in order to get this done.

 

Below I’ve listed the steps required to configure two Workgroup machines so that you can remotely access one from the other using PowerShell.  The computer you’re sitting in front of is called the client machine, while the computer you’re trying to remotely access is called the server machine.