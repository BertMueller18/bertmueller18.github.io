---
layout: post 
title:  "Powershell script with dbatools - Copy Database with Rename" 
date:   2017-10-16T21:44:06.617Z 
categories: powershell sqlserver
link: http://www.sql-aus-hamburg.de/powershell-script-with-dbatools-copy-database-with-rename/ 
tags:
  - links
ogtype: article 
---

> owershell script with dbatools – Copy Database with Rename
 15. March 2017  Björn Peters

Last week I was called to create an automated database copy job, which should refresh a development environment every night with a full backup from the production environment. Here are the given requirements from the customer:

Currently approx. 35 GB
Backup w / copy only
No backup of the backup
Creation of database duplication as an automatic job, attachment, authorization
Daily at 21:21 hour
From: SourceServer, DB instance Source_DatabaseName
To: DestinationServer, DB instance Destination_DatabaseName
Path: DestinantionServer B:\Backup\Source_DatabaseName
Authorization for user: xyz@customerdomain.net
