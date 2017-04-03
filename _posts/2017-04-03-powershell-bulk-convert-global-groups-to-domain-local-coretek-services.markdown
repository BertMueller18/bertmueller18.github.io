---
layout: post 
title:  "PowerShell - Bulk Convert Global Groups to Domain Local... - Coretek Services" 
date:   2017-04-03T08:50:26.188Z 
categories: activedirectory security 
link: http://www.coretekservices.com/2015sep30powershell-bulk-convert-global-groups-domain-local/ 
tags:
  - links
ogtype: article 
---

> PowerShell – Bulk Convert Global Groups to Domain Local…

Recently I was working with someone who spent a bunch of time building Active Directory groups for a project I’m working on.  After he was done, I noticed the groups he made were Global type groups (which is the default type in ADUC) instead of Domain Local type groups, which I needed for my project.

Instead of causing the person to panic, I told him we could turn to PowerShell to easily flip the type.  However, there is one caveat… You cannot convert groups directly from Global to Domain Local, so they have to be converted to Universal first.