---
layout: post 
title:  "Cheat Sheet: Setting Exchange Mailbox User Permissions via PowerShell – Dave Stork's IMHO" 
date:   2017-06-01T22:30:24.923Z 
categories: exchange exchange2016 exchange2013 exchange2010 permissions
link: https://dirteam.com/dave/2015/07/13/cheat-sheet-setting-exchange-mailbox-user-permissions-via-powershell/ 
tags:
  - links
ogtype: article 
---

> Cheat Sheet: Setting Exchange Mailbox User Permissions via PowerShell

One of the things I get asked about quite a lot, is how you can set specific permissions in Exchange Server and Exchange Online. Most cases the Management Console (in 2010) or the Exchange Admin Center (EAC, Exchange 2013 & 2016 and Online) provide most basic permissions like Full Access, Send As and Send On Behalf. However, sometimes an admin has to set Send on Behalf permissions on a Shared Mailbox or disable AutoMapping, those options are not available via EAC. Just as setting specific Folder Permissions within a mailbox.

The solution is to use the Exchange Management Shell, or PowerShell. However, every type of permission has a different cmdlet. If you do not set these permissions on a regular basis, you probably have to look up how to perform these actions. Below are the cmdlets with a specific example, each with a link to the TechNet article explaining in more detail their function (provided you have the correct permissions in order to use them):