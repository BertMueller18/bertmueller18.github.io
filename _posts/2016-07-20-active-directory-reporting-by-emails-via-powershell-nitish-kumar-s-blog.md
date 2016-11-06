---
layout: post 
published: true 
title: "Active Directory Reporting by Emails via Powershell – Nitish Kumar's Blog" 
date: 2016-07-20T05:26:51.597Z 
link: https://nitishkumar.net/2016/07/10/active-directory-reporting-by-emails-via-powershell/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Active Directory Reporting by Emails via Powershell

      4 Votes

Monitoring a large Active Directory environment always comes with so many requirements at times. Some of these might be based on various business requirements while some of them are meant for being proactive over the changes in the environment based on daily activities. All the codes applicable to Windows 2003 environment but should work for higher than that as well.

Let’s visit some of the Powershell scripts which might come useful at times:

Dump of all AD User’s info + group Membership of each user along with all relevant attributes

The below code isn’t sending HTML email, but plain text with two attachments only. We can schedule the same weekly basis or fortnight basis to keep snapshots of AD on regular basis to refer at any point of time in cases of requirement.

