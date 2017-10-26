---
layout: post 
title:  "Migrate SQL Server Logins with PowerShell" 
date:   2017-10-16T21:41:14.412Z 
categories: powershell sqlserver 
link: https://www.mssqltips.com/sqlservertip/4654/migrate-sql-server-logins-with-powershell/ 
tags:
  - links
ogtype: article 
---

> Migrate SQL Server Logins with PowerShell

By: Rajendra Gupta   |   Read Comments   |   Related Tips: More > Security


Attend these FREE SQL Server 2017 webcasts >> click to register


Problem
As a DBA we often have a need to migrate SQL Server logins, permissions, server roles, etc. from one server to another. There are various approaches like using sp_help_revlogin, SSIS, Copy Database Wizard, etc. In this tip we will cover a new approach using PowerShell.