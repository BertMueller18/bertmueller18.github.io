---
layout: post 
title:  "Exchange inter-forest migration tips | Hayes Jupe's Blog" 
date:   2017-06-07T21:46:51.331Z 
categories: exchange migration 
link: http://www.hayesjupe.com/exchange-interforest-migration-tips/ 
tags:
  - links
ogtype: article 
---

> Exchange inter-forest migration tips
Updated on :  15/01/2016
Relevant to:   Exchange 2010/2013/2016
Forest, including exchange, migrations seemed to be something I was doing every month back in the Exchange 2000/2003 days, but then they seemed to stop…. For a while.
 
Recently, in my market, there has been a bit of a spate of them again though – and searching around there are plenty of articles, but none of which I would consider comprehensive, so… this is my bash at it.
 
Tools you will need
ADMT – https://connect.microsoft.com/site1164/program8540
 
Scenario
This post will cover off the following scenarios
·         Two existing org’s merge and wish to link their mailboxes into a new resource forest, with the goal of completely migrating into the new forest over time
o   For the sake of simplicity, this document will refer to
o   DomainA.com – a company with existing AD and exchange (which has merged with DomainB.local)
o   DomainB.local – a company with existing AD and exchange (which has merged with DomainA.com)
o   Resource.com – a forest created representing the new “merged” company name