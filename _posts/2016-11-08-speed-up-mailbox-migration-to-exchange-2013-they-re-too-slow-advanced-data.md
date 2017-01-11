---
layout: post
published: true
title: "Speed up mailbox migration to Exchange 2013 – They’re too slow! | Advanced Data"
date: 2016-11-08T11:52:15.583Z
categories: exchange exchange2013
link: http://www.adnsolutions.com/speed-up-mailbox-moves-to-exchange-2013-theyre-too-slow/
tags:
  - links
ogtype: article
bodyclass: post
---

## Speed up mailbox migration to Exchange 2013 – They’re too slow!
by Brian Scheewe | Aug 28, 2015 | Exchange, Microsoft | 3 comments
Moving mailboxes from Exchange 2007 or 2010 to Exchange 2013 can often go very slowly, even when the network and server resources are fast and abundant!  The Exchange Mailbox Replication Service (MRS) has extensive resource throttling enabled by default in order to prevent mailbox moves from choking out the rest of the users.  Because of this you may see mailboxes with a status of RelinquishedWlmStall and if you look at the details of the Get-MoveRequestStatistics report you will see mailboxes have a lot of time sitting idle under the TotalStalledDueToWriteThrottle counte
