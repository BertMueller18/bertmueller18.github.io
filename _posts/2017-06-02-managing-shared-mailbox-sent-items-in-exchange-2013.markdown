---
layout: post 
title:  "Managing Shared Mailbox Sent Items in Exchange 2013" 
date:   2017-06-01T22:22:50.385Z 
categories: exchange exchange2013 sharedmailbox
tags:
  - links
ogtype: article 
---

> Managing Shared Mailbox Sent Items Behaviour in Exchange Server 2013 and Office 365
JUNE 25, 2015   BY PAUL CUNNINGHAM
With the recent release of Cumulative Update 9 for Exchange Server 2013, as well as updates to Exchange Online (Office 365), Microsoft has made it possible to control the sent items behaviour for shared mailboxes when delegates send mail as the mailbox, or on behalf of the mailbox.

This functionality has been available for quite some time in Exchange Server 2010 (click here for more details) but has been implemented differently in Exchange 2013 and Exchange Online. You will also notice as you read the examples below that managing the settings in a co-existence environment doesn’t follow the normal rules of only using the matching version of management tools to manage a mailbox (eg Exchange 2010 tools to manage an Exchange 2010 mailbox).

Let’s take a look at a how this functionality can be managed in an environment that has all of the following Exchange versions co-existing:

Exchange Server 2010 SP3
Exchange Server 2013 CU9
Exchange Online (Hybrid configuration)
