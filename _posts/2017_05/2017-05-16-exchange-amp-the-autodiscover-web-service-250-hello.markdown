---
layout: post 
title:  "Exchange &amp; The Autodiscover Web Service – 250  Hello" 
date:   2017-05-16T20:49:20.010Z 
categories: exchange autodiscover xml outlook scp
link: https://blogs.technet.microsoft.com/rmilne/2011/10/21/exchange-the-autodiscover-web-service/ 
tags:
  - links
ogtype: article 
---

> Exchange & The Autodiscover Web Service
★★★★★★★★★★★★★★★
Rhoderick Milne [MSFT]21 October, 201112 
0
0
In the Exchange 2003 world and below, those administrators looking to automate and control the behaviour of MAPI profiles on user’s desktops quickly became familiar with tools like:

ORK (Office Resource Kit)
.PRF Files
.OPS files (from the Office Profile wizard)
PROFGEN
PRFPATCH
ExProfRe
 

For a refresher on such joys  of .PRF files etc. take a peek at:

Whitepaper: Configuring Outlook Profiles by Using a PRF File

Automate Outlook Profile Creation Using PRFPATCH

The Exchange Profile Update tool

 

Owch, those were some painful days!  Thankfully with Exchange 2007/2010 and Outlook 2007/2010 we are able to move on from such tasks.  Exchange 2007 introduced the Autodiscover web service which is used by Outlook 2007 and above to automatically configure the required Outlook settings.  This not only includes the initial connection to Exchange but also if the administrator then makes changes to URLs then Outlook will detect and apply such changes.  This is a great boon to administrators and will reduce user & configuration issues.

Sounds good does it not?