---
layout: post 
title:  "Active Directory Script Highlight: Disable and Move Users Who Have Not Logged on In 180 Days | VirtuallyAware" 
date:   2018-04-16T08:51:17.994Z 
categories: activedirectory maintenance powershell
link: https://virtuallyaware.wordpress.com/2018/02/22/active-directory-script-highlight-disable-and-move-users-who-have-not-logged-on-in-180-days/ 
tags:
  - links
ogtype: article 
---

> Active Directory Script Highlight: Disable and Move Users Who Have Not Logged on In 180 Days
Posted on February 22, 2018 by VirtuallyAware
In my last post I showed a simple script to identify users that have not logged on in the last 180 days and export basic information to a CSV file.  This allowed you to look through the list and determine if the users were valid and really did include the users that you wanted to target for disabling.  Once you are comfortable with the users you are targeting, it’s time to disable them.  The following script will again set the population that is over 180 days since last logon, then disable them, then move them to a designated disabled users OU.