---
layout: post 
title:  "Backup SQL Server Databases in Parallel with PowerShell" 
date:   2017-10-30T14:03:32.401Z 
categories: sqlserver maintenance backup
link: https://www.mssqltips.com/sqlservertip/4974/backup-sql-server-databases-in-parallel-with-powershell/ 
tags:
  - links
ogtype: article 
---

> Backup SQL Server Databases in Parallel with PowerShell

By: Pablo Echeverria   |   Read Comments (3)   |   Related Tips: More > PowerShell


Attend these FREE MSSQLTips webcasts >> click to register


Problem
I have a need to decrease the time my SQL Server database backups are taking to run.  I thought about trying to run multiple backups at the same time to see if that would work.  I could have created multiple SQL Server Agent Jobs to run at the same time, but I wanted a more dynamic way to handle this, so I created a PowerShell script that allows processes to run in parallel.

Solution
With PowerShell you can spawn multiple threads to run tasks simultaneously. By implementing this approach using PowerShell, I was able to cut down a process that took over an 1.5 hours to a little over an hour.

