---
layout: post 
title:  "Tracking Active Directory Operations with PowerShell Commands" 
date:   2017-05-16T21:38:53.288Z 
categories: activedirectory security eventlog monitoring
link: http://www.serverwatch.com/server-tutorials/tracking-active-directory-operations-with-powershell-commands.html 
tags:
  - links
ogtype: article 
---

> Tracking Active Directory Operations with PowerShell Commands

By Nirmal Sharma	(Send Email) 
Posted April 24, 2017	
	





There are three operations performed in an Active Directory environment: Create, Modify and Delete. Any Active Directory admin who has sufficient permissions can perform Create, Modify and Delete operations.

The operations can be performed on objects such as users, computers, user and computer properties, contacts, and other objects except critical Active Directory objects. By default, users (including Domain Admins) do not have permissions to perform any operations on critical Active Directory objects.

In an Active Directory environment where there are millions of objects, it sometimes becomes difficult to monitor the changes that have been taken place. Everyday thousands of operations might be taking place.

For example, someone might be creating user accounts, while someone else might be deleting user accounts. Similarly, you might have someone who modifies the user properties.

As a result, it becomes necessary to implement an auditing mechanism that helps you keep track of the Active Directory changes and to help you identify which users made the changes. Windows Server 2008 and earlier operating systems were lacking the capability to report enough details on the changes made in the Active Directory.

However, with Windows Server 2008 R2 and later operating systems, Microsoft now provides more extensive details for Active Directory changes. While you can open the Event Viewer to get the changes that have been taking place throughout Active Directory, it becomes cumbersome when taking a look at each of the events one by one and figuring out the changes that you wish to see.

That's where today's Server Tutorial comes handy. Today we'll talk about the account creation operations you can track by running a simple PowerShell script.