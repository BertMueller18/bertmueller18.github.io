---
layout: post 
title:  "UC Unleashed » Script: New-ExpiringCertificatesReminder.ps1 – Receive a Reminder When Certificates Have Expired/Are Expiring" 
date:   2018-02-11T19:23:06.972Z 
categories: powershell certificate pki automation
link: https://www.ucunleashed.com/1360 
tags:
  - links
ogtype: article 
---

> Script: New-ExpiringCertificatesReminder.ps1 – Receive a Reminder When Certificates Have Expired/Are Expiring
September 14th, 2012Pat RichardLeave a commentGo to comments
Detailed Description
Sometimes we’re so deep in projects or putting out fires that some things just get forgotten, or we don’t get that far down the “to-do” list. Some of those things aren’t that big of a deal and don’t impact users. Other tasks can have drastic impact. Such as forgetting to renew your server certificates. It’s true that some services like the phenomenal Digicert will remind-you-to-death about certs that are expiring. But not all services do that, or they do it once and are forgotten. Other certs, like internal certs, don’t generate a reminder – and some environments don’t allow, or aren’t configured to automatically renew internal certificates. So this lazy, forgetful guy decided to do something about that. A script was born.