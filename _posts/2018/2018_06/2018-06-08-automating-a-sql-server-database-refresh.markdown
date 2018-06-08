---
layout: post 
title:  "Automating a SQL Server Database Refresh" 
date:   2018-06-07T22:00:33.549Z 
categories: sqlserver tsql microsoft powershell
link: https://www.mssqltips.com/sqlservertip/5465/automating-a-sql-server-database-refresh/ 
tags:
  - links
ogtype: article 
---

## Automating a SQL Server Database Refresh

By: Joe Gavin   |   Read Comments (2)   |   Related Tips: More > Restore

FREE MSSQLTips Webcast - "SQL Server 2017 - It Just Gets Faster" - click to register


Problem
You need to automate refreshing a SQL Server database to refresh test or dev, test backups, etc.  In this tip we show how this can be done.

Solution
We can accomplish this with a little PowerShell, a little T-SQL code and SQL Server Agent.

For this tip we have a backup of a database named AutomatedDbRefresh.bak which we will use to automate the restore.  Let's say the backup is done on one server and we want to automate the restore do a different server.