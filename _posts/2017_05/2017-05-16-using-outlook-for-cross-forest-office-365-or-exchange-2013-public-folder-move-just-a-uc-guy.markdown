---
layout: post 
title:  "Using Outlook for Cross Forest (Office 365 OR Exchange 2013) Public Folder move | Just A UC Guy" 
date:   2017-05-16T20:44:45.101Z 
categories: exchange crossforest publicfolder
link: https://justaucguy.wordpress.com/2015/09/15/using-outlook-for-cross-forest-office-365-or-exchange-2013-public-folder-move/ 
tags:
  - links
ogtype: article 
---

> USING OUTLOOK FOR CROSS FOREST (OFFICE 365 OR EXCHANGE 2013) PUBLIC FOLDER MOVE
Why?

Recently a client of mine wanted to consolidate their Public Folder infrastructure, or at least reorganize the existing 2007 version before upgrading to Exchange 2013 with the possibility of Office 365. Cross forest migrations (Exchange 2013 or Office 365) can be tedious to plan, execute and support. Mailbox moves are relatively easy with PowerShell scripts (Prepare-MoveRequest) and cmdlets (New-MoveRequest). However, what is often overlooked is moving Public Folders.
