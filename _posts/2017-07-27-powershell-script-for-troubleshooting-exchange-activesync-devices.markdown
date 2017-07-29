---
layout: post 
title:  "PowerShell Script for TroubleShooting Exchange ActiveSync Devices" 
date:   2017-07-27T19:41:11.458Z 
categories: exchange powershell activesync
link: https://practical365.com/clients/mobile-devices/troubleshooting-exchange-activesync-devices-script/ 
tags:
  - links
ogtype: article 
---

## PowerShell Script for TroubleShooting Exchange ActiveSync Devices
JULY 27, 2017   BY PAUL CUNNINGHAM
On a recent case I was investigating a mobile device that couldn’t connect to a mailbox over ActiveSync. After spending a few minutes collecting information about the mailbox and its associated devices I realized that this task could be performed a lot faster by using a PowerShell script.

Most mobile device troubleshooting cases boil down to one of a few common issues:

AD accounts with permission inheritance disabled
Mailboxes with disabled protocols
Devices blocked by personal block lists, device access rules, or organization policies
EWS block lists (as is the case with Outlook for iOS when it connects using the REST API)
Even though Office 365 MDM and Intune are available, there’s still a lot of usage of ActiveSync out there in the world, especially for on-premises customers. So I am sharing the PowerShell script that I wrote for ActiveSync troubleshooting.