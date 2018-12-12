---
layout: post 
title:  "Three Steps to Migrate Group Policy Between Active Directory Domains or Forests Using PowerShell – GoateePFE – Archived" 
date:   2018-12-12T11:07:57.182Z 
categories: powershell gpo activedirectory
link: https://blogs.technet.microsoft.com/ashleymcglone/2014/04/28/three-steps-to-migrate-group-policy-between-active-directory-domains-or-forests-using-powershell/ 
tags:
  - links
ogtype: article 
---

> Three Steps to Migrate Group Policy Between Active Directory Domains or Forests Using PowerShell
★★★★★★★★★★★★★★★
Ashley McGloneApril 28, 201433 
0
0
Three Steps Ahead
Have you ever wished that you had three legs? Imagine how much faster you could run.  Today we are going to look at three steps to migrating GPOs between domains or forests with PowerShell.  Now that is fast!

The Problem
Have you ever wanted to copy all of your production Group Policy Objects (GPOs) into a lab for testing?  Do you have to copy GPOs between domains or forests?  Do you need to migrate them to another environment due to an acquisition, merger, or divestiture? These are common problems for many administrators.

There are VBScripts provided with the Group Policy Management Console (GPMC), but that is so "last decade". (Really. They were published in 2002.)  What about WMI filters, OU links, login scripts, and embedded credentials? I’ve drafted a PowerShell module to do this with speed and style. This post discusses the pitfalls, preparations, and scripts for a successful GPO migration.

Real-World Scenario
Recently I worked with a customer who had mirrored dev, test, and prod Active Directory forests.  They had the same accounts, groups, OUs, and GPOs in all three places.  Then they had another version of the same dev, test, prod environment for a separate application.  That is two sets of three forests, both with identical GPOs.  Their current process for copying policies was manually backing up and importing the GPOs, which is how TechNet tells you to do it.  At this scale, however, they were in need of an automated solution.  Enter PowerShell.