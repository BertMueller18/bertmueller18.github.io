---
layout: post 
title:  "Automatic Download and Import of Updates into MDT - Aaron Parker" 
date:   2017-12-24T10:11:26.367Z 
categories: mdt wsus automation
link: https://stealthpuppy.com/powershell-download-import-updates-mdt/ 
tags:
  - links
ogtype: article 
---

> Automatic Download and Import of Updates into MDT

A couple of months back, I sent an email to the Microsoft MVP mailing list to see if anyone knew of a JSON feed of Windows 10 updates from Microsoft . I’d found a way to grab the latest Firefox version via PowerShell and was hoping to do something similar for Windows 10. Keith Garner responded with something even better – a working script that pulls from a JSON resource on the Windows 10 and Windows Server 2016 Update History page, to return the most recent cumulative update.