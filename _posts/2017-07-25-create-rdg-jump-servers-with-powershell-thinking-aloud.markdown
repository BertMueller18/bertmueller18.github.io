---
layout: post 
title:  "Create RDG jump servers with PowerShell | Thinking aloud" 
date:   2017-07-25T21:49:48.373Z 
categories: rdsh security windows 
link: https://www.yobyot.com/aws/configure-remote-desktop-gateway-bastion-hosts-with-powershell/2017/07/24/ 
tags:
  - links
ogtype: article 
---

## Configure Remote Desktop Gateway bastion hosts with PowerShell

Set up a Windows jump box in AWS or Azure
Three years ago this month, I described how you can use the Remote Desktop Gateway (RDG) as a Windows bastion, or jump, server to provide secure access to Windows hosts inside a private subnet in either AWS and/or Azure. Here’s a picture of how this works.


Remote Desktop Gateway connections (click to enlarge)
Note that it’s possible for the RDG host to connect to itself. Simply specify the internal address or DNS of the RDG host as the RDP connection destination. I do this all the time as a test — of the configuration as well as my own mind as it’s a bit of a mental twister.

But there’s always been a fly in the ointment of this otherwise standard process: configuring the RDG server itself had to be done via the UI.

