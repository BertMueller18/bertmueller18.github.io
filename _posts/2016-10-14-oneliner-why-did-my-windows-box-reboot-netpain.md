---
layout: post
published: true
title: "Oneliner: Why did my Windows box reboot? – Netpain"
date: 2016-10-14T11:21:18.758Z
categories:  
link: http://netpain.pvz.pp.se/oneliner-why-did-my-windows-box-reboot/
tags:
  - links
ogtype: article
bodyclass: post
---

> Get-WinEvent -LogName System -FilterXPath "*[System[(EventID=1074 or EventID=1076 or EventID=6008)]]" -MaxEvents 1 -ComputerName localhost | fl
