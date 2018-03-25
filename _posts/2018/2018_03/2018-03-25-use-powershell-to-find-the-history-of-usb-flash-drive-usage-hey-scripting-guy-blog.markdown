---
layout: post 
title:  "Use PowerShell to Find the History of USB Flash Drive Usage – Hey, Scripting Guy! Blog" 
date:   2018-03-25T15:23:10.562Z 
categories: powershell automation
link: https://blogs.technet.microsoft.com/heyscriptingguy/2012/05/18/use-powershell-to-find-the-history-of-usb-flash-drive-usage/ 
tags:
  - links
ogtype: article 
---

##  Use PowerShell to Find the History of USB Flash Drive Usage

Summary: Microsoft premier field engineer, Jason Walker, shows how to use Windows PowerShell to get a history of USB drive usage.

Microsoft Scripting Guy, Ed Wilson, is here. I was talking to Jason Walker at the Charlotte Windows PowerShell User Group the other day. I asked him what cool things he was doing with Windows PowerShell, and he discussed a script he had recently written. I encouraged him to write a guest blog about the script. Today’s blog is a result of that conversation.



Jason Walker is a premier field engineer (PFE) at Microsoft, and he supports customers in the public arena. His primary job is supporting Exchange Server, but he jumps at the opportunity to flex his Windows PowerShell muscles to resolve any issue that may come up. It does not matter if it is related to Exchange Server. Jason also actively participates in the Charlotte PowerShell Users Group.

Twitter: AutomationJason

USB ports are an awesome resource to any computer. They allow you quickly connect and use accessories such as mice, keyboards, and storage devices, just to name a few. However, USB storage devices are a popular vector bad guys use to get nefarious code onto a machine. With my customers being in the public sector, security is a top priority, and USB storage devices are not allowed. We could disable USB ports all together, but that would eliminate the ability to use other USB devices. Therefore, users are told to simply not use USB storage devices. The need came up to see if the users are playing by the rules and Windows PowerShell was the answer to that need.