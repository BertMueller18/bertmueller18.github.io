---
layout: post 
title:  "Quickly list all mailboxes to which a particular user has access | Blog" 
date:   2017-05-22T08:05:52.859Z 
categories: exchange powershell permissions
link: http://www.michev.info/Blog/Post/1516/quickly-list-all-mailboxes-to-which-a-particular-user-has-access 
tags:
  - links
ogtype: article 
---

## Quickly list all mailboxes to which a particular user has access
Posted on April 13, 2015 by Vasil Michev
​This question seems to get asked a lot, and people are unaware how easy the answer really is. Here it is:

List all mailboxes to which a particular user has Full Access permissions:
PS C:\> Get-Mailbox | Get-MailboxPermission -User vasil
 
Identity             User                 AccessRights
 
--------             ----                 ------------
HuKu                 Vasil Michev         {FullAccess}
retail               Vasil Michev         {FullAccess}
sharednew            Vasil Michev         {FullAccess}
testplan2            Vasil Michev         {FullAccess}
WC                   Vasil Michev         {FullAccess}