---
layout: post 
published: true 
title: "									Exchange 2016 upgrade tips and tricks from the field (Part 1)  :: Migration &amp; Deployment  :: Exchange 2016 Articles  :: Articles &amp; Tutorials  :: MSExchange.org						" 
date: 2016-07-15T12:29:46.734Z 
link: http://www.msexchange.org/articles-tutorials/exchange-2016-articles/migration-deployment/exchange-2016-upgrade-tips-and-tricks-field-part1.html 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Exchange 2016 upgrade tips and tricks from the field (Part 1)
by Henrik Walther [Published on 12 May 2016 / Last Updated on 12 May 2016]  


In this article, I will provide you with crucial Exchange 2016 upgrade information based on large enterprise organization engagements I have been involved in as an architect since the release of Exchange Server 2016 RTM.

If you would like to be notified of when Henrik Walther releases the next part in this article series please sign up to our MSExchange.org Real Time Article Update newsletter.

Introduction

Most of the customer engagements I have been dealing with have been scenarios where the customer currently was running Exchange 2010 with a wish to either perform an on-premises upgrade to Exchange Server 2016, upgrade to Exchange 2016 and establish an Exchange hybrid with Exchange Online, or establish an Exchange hybrid deployment and migrate all mailboxes to Exchange Online. The latter scenario has also involved deploying Exchange Server 2013 or 2016 hybrid servers because I was dealing with multiple Exchange forests that were going to have an Exchange hybrid established against the same Exchange Online tenant.

Note:
Although a good portion of the information in this article can be used for cross-forest Exchange migrations, this specific scenario is out of scope.

Let’s get going.