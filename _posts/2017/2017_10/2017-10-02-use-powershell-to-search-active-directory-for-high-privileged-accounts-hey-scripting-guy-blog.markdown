---
layout: post 
title:  "Use PowerShell to Search Active Directory for High-Privileged Accounts – Hey, Scripting Guy! Blog" 
date:   2017-10-02T09:48:15.043Z 
categories: powershell activedirectory reporting
link: https://blogs.technet.microsoft.com/heyscriptingguy/2014/11/15/use-powershell-to-search-active-directory-for-high-privileged-accounts/ 
tags:
  - links
ogtype: article 
---

> Use PowerShell to Search Active Directory for High-Privileged Accounts
★★★★★★★★★★★★★★★
The Scripting GuysNovember 15, 20140 
0
0
Summary: Microsoft PFE, Ian Farr, provides a Windows PowerShell function that searches for Active Directory users with high-privileged memberships.

Microsoft Scripting Guy, Ed Wilson, is here. Today, we have another guest blog post from Microsoft premier field engineer (PFE), Ian Farr. Take it away, Ian…

As a youngster, I loved watching Columbo, the bumbling, disheveled, and tenacious LAPD detective. At the end of each episode, almost as an afterthought, he’d outwit the murderer with an investigative coup de grace. Televisual gold!

A few months ago, I discussed a function that analyzes the authentication of read-only domain controllers (RODCs). It reports on accounts authenticated by an RODC that aren’t "revealed,"—that is, the account password or secret is not stored on the RODC. For the full write up, see Use PowerShell to Work with RODC Accounts.