---
layout: post 
title:  "Running PowerShell in a SQL Agent Job - SQL Hammer | SQL Hammer" 
date:   2017-12-15T08:41:02.092Z 
categories: sqlserver
link: https://www.sqlhammer.com/running-powershell-in-a-sql-agent-job/ 
tags:
  - links
ogtype: article 
---

> Running PowerShell in a SQL Agent Job
4th March 2015Derik HammerAdministration 6 Comments
When creating a SQL Agent Job to execute a PowerShell script, you have to decide which way that you want the PowerShell to run. Depending upon which version of SQL Server that you are using and which job step type that you choose, you might be running in different versions of PowerShell with different execution policies. I will demonstrate the behaviors.