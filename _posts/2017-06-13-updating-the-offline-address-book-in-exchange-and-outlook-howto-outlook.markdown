---
layout: post 
title:  "Updating the Offline Address Book in Exchange and Outlook - HowTo-Outlook" 
date:   2017-06-13T20:46:50.286Z 
categories: exchange exchange2013 oab
link: https://www.howto-outlook.com/howto/oabupdate.htm#oabregistryoutlook 
tags:
  - links
ogtype: article 
---

> Updating the Offline Address Book in Exchange and Outlook

When you have Cached Exchange Mode enabled, Outlook by will by default cache the main Global Address List as well. This is called the Offline Address Book and is being generated on the Exchange server.

Due to various synching schedules, it can take up to 48 hours before you could actually see a change in Outlook after a modification has been made on the Exchange server or in Active Directory.

In this guide, the relevant timings are explained and instructions are given in how you can directly force an update and resync, which can be very handy when troubleshooting or when you work in an Exchange environment which sees a lot of user mailbox mutations.


The automatic sync and update schedules
Updating Outlook manually
Modify the OAB update frequency in Outlook
Modify the OAB download behavior in Outlook
Location of the cached oab-files
Modify default maintenance schedule in Exchange
Force OAB update and redistribution on Exchange
