---
layout: post 
title:  "List of active mailboxes (PowerShell)" 
date:   2017-06-07T22:11:44.520Z 
categories: exchange powershell inventory
link: https://www.codetwo.com/admins-blog/list-of-active-mailboxes-powershell/?utm_source=dlvr.it&utm_medium=twitter 
tags:
  - links
ogtype: article 
---

> List of active mailboxes (PowerShell)
Posted on April 24, 2017
by Adam the 32-bit Aardvark
Thanks to PowerShell, you can easily verify the activity on a shared or a user’s mailbox on Exchange (on-premises and Online).

The cmdlets that come in handy in this situation are:

`Get-MailboxStatistics`, which lets us check the Last logon time on a mailbox,
And, of course, `Get-Mailbox`



Let’s start with the most basic activity report – a list of users’ and shared mailboxes sorted starting from the most recent logon time.

