---
layout: post 
published: true 
title: "Cyber Defense | PowerShell Script to Block Cortana for Privacy | SANS Institute" 
date: 2016-08-23T13:42:29.981Z 
link: https://cyber-defense.sans.org/blog/2016/08/20/powershell-script-to-block-cortana-for-privacy 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> PowerShell Script to Block Cortana for Privacy
0 comments Posted by Jason Fossen
Filed under Course SEC505, Jason Fossen, PowerShell
-

Privacy advocates dislike the amount of personal information shared with Microsoft through the Cortana search feature.

In Windows 10 version 1607 (the "Anniversary Update" released in August 2016) Microsoft removed the easy-to-find on/off switch for Cortana, but at least there is a registry value named "AllowCortana" that can be set to zero to disable Cortana.

But will this registry value block all of Cortana's Internet usage? Unknown, but we can also use the built-in Windows Firewall to block all outbound Cortana network traffic too, just in case.