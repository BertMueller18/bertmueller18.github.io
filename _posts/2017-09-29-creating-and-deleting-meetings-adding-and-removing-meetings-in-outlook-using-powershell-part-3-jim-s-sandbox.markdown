---
layout: post 
title:  "Creating and Deleting Meetings: Adding and removing meetings in Outlook using PowerShell part 3 | Jim’s Sandbox" 
date:   2017-09-29T19:10:26.449Z 
categories: exchange powershell ews 
link: http://jeestirling.info/wp/2015/02/14/creating-and-deleting-meetings-adding-and-removing-meetings-in-outlook-using-powershell-part-3/ 
tags:
  - links
ogtype: article 
---

> Creating and Deleting Meetings: Adding and removing meetings in Outlook using PowerShell part 3
Posted on Saturday, 14 February, 2015
In the previous post Getting PowerShell ready to work with Exchange: Adding and removing meetings in Outlook using PowerShell part 2 we looked at preparing the script to create meetings in an Exchange calendar. Now that the connection has been created to the appropriate calendar we can start creating meetings (which is the easy bit) and deleting them when necessary (which is not so easy).

There are a number of tutorials on using PowerShell to create a meeting in an Exchange calendar, and include the necessary participants.  Two I found particularly helpful were Aman Dhally’s Powershell and Outlook: Create Calendar Meetings using Powershell function and Mike Pfeiffer’s Creating Calendar Items with PowerShell and the EWS Managed API (which includes an interactive script that is great for testing).

In our case the details of the appointment were captured through a separate system and held in a SQL Server table.  The script used a view of that table to select the appointments that had not yet been processed and read them into an ADO.net data table. This is not really the focus of this series of posts so I have not included the detail of accessing the data from the database not of constructing the body of the meeting record using token substitutions. Instead we will focus on the mechanics of creating a meeting record.