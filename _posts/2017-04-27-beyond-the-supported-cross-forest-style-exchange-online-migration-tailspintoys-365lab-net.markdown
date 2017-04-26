---
layout: post 
title:  "Beyond the supported – Cross forest style Exchange Online Migration | Tailspintoys – 365lab.net" 
date:   2017-04-26T22:05:23.653Z 
categories: exchange migration
link: https://365lab.net/2017/01/08/beyond-the-supported-cross-forest-style-exchange-online-migration/ 
tags:
  - links
ogtype: article 
---

> Beyond the supported – Cross forest style Exchange Online Migration
1 Reply
Migration and consolidation projects always put our skills to the test and in some cases forces us to do things that are not fully supported. But sometimes, the end justifies the means.

Some time ago, I did an Exchange Online onboarding project in a quite complex scenario, at least in terms of the identities. 10+ Active Directories and almost as many Exchange environments. On top of that, due to several reasons, it was not possible to create trusts between the different directories. Not the easiest starting point…
Looking at all different options we agreed upon to synchronize one of the directories to Azure AD. This meant that all users not in that directory were to get new accounts, effectively taking the first step towards a common environment.

– Identites – check!

The next step were to determine the migration strategy for the Exchange environments that was ranging from Exchange 2007 -> 2013. Given the quite complex scenario without trusts between the environments, our minds were set to use a third-party tool to do all the migrations. I always like challenging the obvious path, so I wanted to see if it was possible to do native mailbox moves even though there was no possibility to use the regular Hybrid Configuration Wizard.