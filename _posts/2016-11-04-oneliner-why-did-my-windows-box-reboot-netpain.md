---
layout: post 
published: true 
title: "Oneliner: Why did my Windows box reboot? – Netpain" 
date: 2016-11-04T10:29:13.891Z 
link: http://netpain.pvz.pp.se/oneliner-why-did-my-windows-box-reboot/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Oneliner: Why did my Windows box reboot?

Ever found yourself wanting to quickly figure out why a windows box rebooted? Just drop this beauty into Powershell:

Get-WinEvent -LogName System -FilterXPath "*[System[(EventID=1074 or EventID=1076 or EventID=6008)]]" -MaxEvents 1 -ComputerName localhost | fl

If you want to check against a remote computer, just change out “localhost” for the computer of your choice.

tl;dr: Reading the output will make it clear what happened to the machine.