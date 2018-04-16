---
layout: post 
title:  "Active Directory Script Highlight: Identify Old Computer Objects Before AD Migrations | VirtuallyAware" 
date:   2018-04-16T08:49:41.164Z 
categories: activedirectory powershell migration
link: https://virtuallyaware.wordpress.com/2018/03/19/active-directory-script-highlight-identify-old-computer-objects-before-ad-migrations/ 
tags:
  - links
ogtype: article 
---

## Active Directory Script Highlight: Identify Old Computer Objects Before AD Migrations
Posted on March 19, 2018 by VirtuallyAware
In the last of my Active Directory cleanup post, I have given you some options to identify, disable, and move User objects based on a certain time of inactivity.  In this post I am going to give you some simple scripts to do the same thing for your Computer objects.  The hope it that by following these posts you will be left with the real target of objects to be migrated, or to give your Active Directory a good spring cleaning that often gets neglected in the day to day management of your environments.

The first script will give some basic information back on Computer Objects that have not set their computer password in the last 180 days that are not already disabled.  Output gives SamAccountName, LastPasswordSet, Name, DistinguishedName, and confirmation that the Computer Object is enabled.   Sorts the output by LastLogonDate attribute and Exports the output to a CSV location.  This is a broad sweep to get an idea of what is out there so you can make determinations about location and age of Computer Objects.