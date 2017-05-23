---
layout: post 
title:  "PowerShell: Filter by User when Querying the Security Event Log with Get-WinEvent and the FilterHashTable Parameter – Mike F Robbins" 
date:   2017-05-23T21:50:00.394Z 
categories: windows eventlog powershell security
link: http://mikefrobbins.com/2015/10/01/powershell-filter-by-user-when-querying-the-security-event-log-with-get-winevent-and-the-filterhashtable-parameter/ 
tags:
  - links
ogtype: article 
---

> PowerShell: Filter by User when Querying the Security Event Log with Get-WinEvent and the FilterHashTable Parameter

MIKE F ROBBINS OCTOBER 1, 2015 2
I recently ran across something interesting that I thought I would share. The help for the FilterHashTable parameter of Get-WinEvent says that you can filter by UserID using an Active Directory user account’s SID or domain account name: