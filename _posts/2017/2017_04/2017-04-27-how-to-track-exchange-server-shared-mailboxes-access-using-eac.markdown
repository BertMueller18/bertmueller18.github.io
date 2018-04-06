---
layout: post 
title:  "How to track Exchange Server Shared Mailboxes Access using EAC" 
date:   2017-04-27T14:39:12.456Z 
categories: exchange security monitoring
link: https://www.lepide.com/how-to/track-shared-exchange-mailboxes-access.html 
tags:
  - links
ogtype: article 
---

> Track shared mailbox access on Exchange Server
In many organizations you will commonly find multiple users accessing the same mailboxes, which can lead to some users having unauthorized access to sensitive data. It is very important to have suitable monitoring mechanisms in place to make sure that only those with the correct permissions have access to the correct data in shared mailboxes. PowerShell cmdlets enable tracking of shared mailbox access. Using PowerShell cmdlets you can enable mailbox auditing and then view the audit reports in the Exchange Admin Center.

With the launch of Exchange Server 2013, audit reports can be accessed through the Exchange admin center (EAC) too. In this article, we will show you show to generate these reports using PowerShell commands and view them using the EAC.