---
layout: post 
published: true 
title: "Step-By-Step: Identifying Large Exchange Mailbox Folders Via PowerShell | CANITPRO" 
date: 2016-05-10T07:05:30.134Z 
categories: exchange exchange2013
link: https://blogs.technet.microsoft.com/canitpro/2016/03/23/step-by-step-identifying-large-exchange-mailbox-folders-via-powershell/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Step-By-Step: Identifying Large Exchange Mailbox Folders Via PowerShell
March 23, 2016 By MVP Thomas Rayner0

Identifying users with large Exchange mailboxes is a task undertaken by most system administrators who are in need of freeing up space on their mail servers. While most search for mailboxes approaching a certain size, I wanted to take this a step further and identify the large folders within user mailboxes. An example of this would be to find all the users who have a large Deleted Items folder or Sent Items or Calendar that would be eligible to be cleaned out. It’s made to be run from a Remote Exchange Management Shell connection instead of by logging into an Exchange server via remote desktop and running such a shell manually.