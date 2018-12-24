---
layout: post 
title:  "PowerShell: Documenting your environment by running systeminfo on all Domain-Computers – SID-500.COM" 
date:   2018-11-03T22:18:38.931Z 
categories: windows inventory powershell
link: https://sid-500.com/2017/08/09/powershell-documenting-your-environment-by-running-systeminfo-on-all-domain-computers/ 
tags:
  - links
ogtype: article 
---

> PowerShell: Documenting your environment by running systeminfo on all Domain-Computers
BY PATRICK GRUENAUER ON 9. AUGUST 2017	• ( 8 COMMENTS )
Systeminfo gives you a perfect overview of your system. But what about the other systems in your domain? Sure, you can use 3rd Party Tools or SCCM. But the number of those who can´t use enterprise software is greater than you think. In this article I am going to describe how to run systeminfo on all Client Computer without using 3rd Party Tools.

What is systeminfo?

Open PowerShell. Type systeminfo.