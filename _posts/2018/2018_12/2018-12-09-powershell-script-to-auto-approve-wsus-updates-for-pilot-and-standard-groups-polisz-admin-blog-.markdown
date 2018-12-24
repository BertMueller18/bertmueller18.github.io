---
layout: post 
title:  "PowerShell script to auto approve WSUS updates for pilot and standard groups. – Polisz Admin Blog " 
date:   2018-12-09T21:23:34.111Z 
categories: wsus powershell windows automation
link: https://paweljarosz.wordpress.com/2016/12/24/powershell-script-to-auto-approve-wsus-updates-for-pilot-and-standard-groups/ 
tags:
  - links
ogtype: article 
---

## PowerShell script to auto approve WSUS updates for pilot and standard groups.

Recently there has been a need for me to create script that will cover auto approval work for WSUS.

So the idea was tu approve certain patches to pilot group, and after 2 weeks apply these on standard target group and do another pilot group approval for latest time span.

Important! WSUS target groups need to have “Standard” and “Pilot” in their names.

