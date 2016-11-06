---
layout: post 
published: true 
title: "LazyWinAdmin: PowerShell Tip - Generate a list of Mac Addresses" 
date: 2016-09-26T19:24:27.458Z 
link: http://www.lazywinadmin.com/2016/08/powershell-tip-generate-list-of-mac.html?utm_content=buffer8a908&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> PowerShell Tip - Generate a list of Mac Addresses

While playing in my lab I needed to create a bunch of fake Devices in System Center Configuration Manager (SCCM). When creation devices you need two pieces of information, the computer name and the Mac Address of the device.

I used the following method to generate my list of mac addresses.

# First, get a list of mac address.
1..150 | ForEach-Object { '{0:X12}' -f $_ }
# Second step: Before we import we need to add a colon ":" every two characters
1..150|%{((('{0:X12}' -f $_) -split '(..)')|?{$_}) -join ":"}