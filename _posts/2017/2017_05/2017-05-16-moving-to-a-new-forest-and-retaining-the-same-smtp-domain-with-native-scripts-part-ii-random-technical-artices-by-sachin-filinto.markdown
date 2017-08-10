---
layout: post 
title:  "Moving to a new forest and retaining the same SMTP domain ( with native scripts ) – Part II – Random Technical Artices By Sachin Filinto" 
date:   2017-05-16T20:41:45.583Z 
categories: exchange crossforest 
link: https://blogs.technet.microsoft.com/sachinf/2013/01/08/moving-to-a-new-forest-and-retaining-the-same-smtp-domain-with-native-scripts-part-ii/ 
tags:
  - links
ogtype: article 
---

> Moving to a new forest and retaining the same SMTP domain ( with native scripts ) – Part II
★★★★★★★★★★★★★★★
Sachin FilintoJanuary 8, 20133 
0
0
 
3. Moving the Active Directory account using ADMT
ADMT is a great tool for Migrating and Restructuring Active Directory Domains ( user accounts, passwords, groups & group membership, computer accounts & much more.)

However It is very important to note that ADMT DOES NOT touch Exchange attributes.

ADMT can be executed before prepare-move request, after prepare-move request or skipped if we want to use a linked account.

Assuming Prepare-move request was executed first, when executing ADMT we need to merge the account with an existing MEU.

Below are screen grabs of the ADMT wizard. the critical options are highlighted