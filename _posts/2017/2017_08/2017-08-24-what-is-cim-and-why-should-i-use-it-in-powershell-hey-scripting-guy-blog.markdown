---
layout: post 
title:  "What is CIM and Why Should I Use It in PowerShell? – Hey, Scripting Guy! Blog" 
date:   2017-08-24T05:33:34.392Z 
categories: wmi cim powershell
link: https://blogs.technet.microsoft.com/heyscriptingguy/2014/01/27/what-is-cim-and-why-should-i-use-it-in-powershell/ 
tags:
  - links
ogtype: article 
---

## What is CIM and Why Should I Use It in PowerShell?

Summary: Honorary Scripting Guy and guest blogger, Trevor Sullivan, explores CIM and using it with Windows PowerShell.

Microsoft Scripting Guy, Ed Wilson, is here. Today we have a guest post from Trevor Sullivan. Trevor is an Honorary Scripting Guy and a recognized Microsoft Community Contributor (MCC). To see more of Trevor’s guest posts, see these Hey, Scripting Guy! Blog posts. You can reach Trevor on Twitter (https://twitter.com/pcgeek86) or follow him on his blog, Trevor Sullivan's Tech Room, Minding the gap between administration and development.

Note  This is the first in a series of five posts by Trevor where he will talk specifically about using the CIM cmdlets. Today’s post provides a bit of background about CIM and explains why you will want to use this exciting technology.

Now, here’s Trevor…

For a long time, Microsoft has had a technology called Windows Management Instrumentation (WMI) built into the Windows operating system. WMI is built on the WBEM and CIM standards from the Distributed Management Task Force (DMTF). System information at the hardware and software layers is exposed via a standard interface through WMI. The net result of this is the ability to easily view, and sometimes modify, system information and configuration settings.

As described by the DMTF, “CIM provides a common definition of management information for systems, networks, applications and services, and allows for vendor extensions. CIM's common definitions enable vendors to exchange semantically rich management information between systems throughout the network.”