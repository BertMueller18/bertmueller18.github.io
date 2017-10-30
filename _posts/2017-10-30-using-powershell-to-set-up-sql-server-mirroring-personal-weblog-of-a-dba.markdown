---
layout: post 
title:  "Using Powershell to Set Up SQL Server Mirroring | Personal Weblog of a DBA" 
date:   2017-10-30T22:29:37.322Z 
categories: powershell sqlserver
link: http://www.webofwood.com/2010/07/29/powershell-sqlserver-mirroring/ 
tags:
  - links
ogtype: article 
---

> 
Using Powershell to Set Up SQL Server Mirroring
5 Replies
Management recently decided to use database mirroring as our DR solution. Because mirroring is done at the database level and not at the server level, I had a lot, a very lot of databases to be mirrored. To make it easier I decided to cobble together a simplistic script to do this.

I typically use a ‘management’ server for most of my needs and have therefore written the script to use UNC type pathing for the primary as well as mirror server. You will also notice I defaulted several of the parameters. This is handy when working on a set of servers for multiple databases.