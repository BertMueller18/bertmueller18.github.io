---
layout: post
published: true
title: "PowerShell Solutions - Several tips for daily tasks  - SQLServerCentral"
date: 2016-10-06T08:09:52.616Z
categories: powershell programming 
link: http://www.sqlservercentral.com/articles/Datafile/145674/
tags:
  - links
ogtype: article
bodyclass: post
---

## PowerShell Solutions - Several tips for daily tasks
By Daniel Calbimonte, 2016/09/27

Introduction
In this article we will learn how to monitor the size of data and transaction log files in SQL Server and how to backup log files if they exceed a specified size in PowerShell.

If you do not have any experience at all in PowerShell, this article is for you. If you have some experience with PowerShell, you may find some very interesting tips in this article that you did not know.

We will do the following:

Detect all the data files and transactional log files of a specified size.
How to display the size of files in MB, GB (by default they are in bytes)
Learn how to do a full and transactional log backup in PowerShell using specific cmdlets.
Learn how to run any SQL script in PowerShell.
Detect databases with Full Recovery Model (because you cannot do a transaction log backup in a database with simple recovery model).
 Learn how to backup the transaction log of all the databases with full recovery mod
