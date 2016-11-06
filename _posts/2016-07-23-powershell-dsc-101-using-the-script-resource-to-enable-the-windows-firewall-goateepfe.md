---
layout: post 
published: true 
title: "PowerShell DSC 101: Using the Script Resource to Enable the Windows Firewall – GoateePFE" 
date: 2016-07-23T20:39:25.083Z 
link: https://blogs.technet.microsoft.com/ashleymcglone/2016/07/21/powershell-dsc-101-using-the-script-resource-to-enable-the-windows-firewall/?utm_content=bufferb8418&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> PowerShell DSC 101: Using the Script Resource to Enable the Windows Firewall
Learning PowerShell Desired State Configuration
PowerShell DSC is one of my favorite topics to teach, because the technology is simply amazing. Usually I do not have enough time with a customer to teach all of the built-in resources. I would guess that the Script resource is one of the least understood. Today’s post outlines a simple example to enable the Windows Firewall. This sample will work on Windows Server 2008 R2 and above.

Automating Your Server Build Sheet
Last week I was on site with a customer doing a PS DSC POC (PowerShell Desired State Configuration Proof of Concept). We took their server build check sheet, identified DSC resources for each step, and then began converting their manual server config process into PowerShell DSC.

The customer was new to DSC and requested a sample of how they could use the built-in Script resource. One of the items on the build sheet was to make sure the Windows Firewall was turned on. This was the perfect opportunity for a Script resource example.