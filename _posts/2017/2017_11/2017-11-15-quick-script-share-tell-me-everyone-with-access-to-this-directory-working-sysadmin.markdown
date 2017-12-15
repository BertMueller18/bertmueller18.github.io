---
layout: post 
title:  "Quick Script Share: Tell Me Everyone With Access To This Directory – Working Sysadmin" 
date:   2017-11-15T07:30:18.689Z 
categories: powershell programming security 
link: http://www.workingsysadmin.com/quick-script-share-tell-me-everyone-with-access-to-this-directory/ 
tags:
  - links
ogtype: article 
---

## Quick Script Share: Tell Me Everyone With Access To This Directory

September 16, 2015active directory, PowerShell, PowerShell ISEisesteroids, powershell, powershell ise, quick script sharing, quick tip
Trying something new. Here’s a quick script I threw together to satisfy a request along the lines of “tell me all the users who have access to this directory”. It’s easy to see all the groups that have access just by right-clicking a directory and going to the Security tab but it’s a pain to get all the users who belong to those groups – especially if there are nested groups (within nested groups, within nested groups). Hence, this script. In addition to the ActiveDirectory PowerShell module, you of course need to be able to read the ACL on the directory you are interested in so use your admin account.

In this experimental post, I’m not going to break down the script, but instead, I’ve quickly commented in-line most of the tricky bits. I think it’s pretty straight forward, but, I wrote it. Let me know what you think.