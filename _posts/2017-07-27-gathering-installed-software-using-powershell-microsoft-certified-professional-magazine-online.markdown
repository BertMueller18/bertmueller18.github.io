---
layout: post 
title:  "Gathering Installed Software Using PowerShell -- Microsoft Certified Professional Magazine Online" 
date:   2017-07-27T19:39:20.680Z 
categories: powershell automation winrm remoting
link: https://mcpmag.com/articles/2017/07/27/gathering-installed-software-using-powershell.aspx 
tags:
  - links
ogtype: article 
---

> Gathering Installed Software Using PowerShell
There's two ways to accomplish this task: the wrong way and the right way. Here's how to do both.

By Boe Prox07/27/2017
If there is one thing an administrator finds themselves doing, it is probably determining what software is installed on their system. It could be simply for just knowing what they have installed, or determining if some software installed may have vulnerabilities which are fixed via a security update or performing an audit for software (which may not have been approved to be installed). Either way, having a means to locate this software can be difficult if you do not have tools like SCCM or another third-party tool available to perform this type of audit.

PowerShell can help us in gathering the software on a local or remote system by giving us a couple of different options to perform the software gathering. One is through WMI and another is by looking in the registry.

