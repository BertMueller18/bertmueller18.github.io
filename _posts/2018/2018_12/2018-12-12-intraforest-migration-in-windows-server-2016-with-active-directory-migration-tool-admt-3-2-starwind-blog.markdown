---
layout: post 
title:  "Intraforest Migration in Windows Server 2016 with Active Directory Migration Tool (ADMT) 3.2 | StarWind Blog" 
date:   2018-12-12T11:03:24.693Z 
categories: admt migration powershell activedirectory
link: https://www.starwindsoftware.com/blog/intraforest-migration-in-windows-server-2016-with-active-directory-migration-tool-admt-3-2 
tags:
  - links
ogtype: article 
---

> Intraforest Migration in Windows Server 2016 with Active Directory Migration Tool (ADMT) 3.2
Posted by Karim Buzdar on May 23, 2017	
Tags: Active Directory Migration Tool, AD, ADMT, ADMT console, ADMT Snap-in, Domain Controller, object migration, PowerShell, windows server 2016
00080
Introduction
In this first blog post, I’ll walk you through to migrate Active Directory objects (users, groups, and workstations or member servers) between two domains in the same forest (Intraforest) using Active Directory Migration Tool (ADMT) 3.2.

ADMT allows you to migrate objects (including users, groups, computers, profiles, service and managed service accounts) with the help of the following tools:

ADMT console
Command line
VBScript
However, in this post, I’ll focus only on ADMT console and command line.