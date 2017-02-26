---
layout: post 
title:  "	Just can't get enough of IT | Make a disconnected mailbox visible" 
date:   2017-02-26T08:11:16.886Z 
categories: exchange exchange2016 exchange2013 powershell
link: https://www.granikos.eu/de/justcantgetenough/PostId/280/make-a-disconnected-mailbox-visible 
tags:
  - links
ogtype: article 
---

> MAKE A DISCONNECTED MAILBOX VISIBLE
On January 11, 2017 Thomas Stensitzki 0 Comment Exchange 2013 Exchange Server 163 Views
When you delete a mailbox or an Active Directory account, the soft-deleted or disconnected mailbox won't show up in the list of disconnected mailboxes immediately. The mailbox status is updated as part of a mailbox store maintenance task.

When you query a mailbox database for disconnected mailboxes you will find a mailbox having the DisconnectReason and DisconnectDate attribute empty.