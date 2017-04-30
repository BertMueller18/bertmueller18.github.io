---
layout: post 
title:  "Exchange PowerShell: How to list all SMTP email addresses in Exchange - Oxford SBS Guy" 
date:   2017-04-30T11:36:42.449Z 
categories: exchange powershell inventory
tags:
  - links
ogtype: article 
---

> xchange PowerShell: How to list all SMTP email addresses in Exchange
11 Replies


In my last Exchange PowerShell post i looked at listing users hidden from the Global Address List. In this post we’ll look at listing all email addresses in use in Microsoft Exchange. This can be useful if you are trying to add an email address and you get an error message because it is already in use somewhere.

Although email addresses are most often associated with mailboxes, they can be found in other items too. In Exchange, Contacts and Distribution lists also have email addresses (as do Public Folders which we’ll look at another time). For that reason we can’t use Get-Mailbox which we used in the last post as that will limit our search to mailboxes only, instead we’ll be using Get-Recipient.


If you pipe Get-Recipient into Get-Member you will see an EmailAddresses property which is exactly what we are after. As you can see below GM is an alias of Get-Membe