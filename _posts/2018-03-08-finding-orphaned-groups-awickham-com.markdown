---
layout: post 
title:  "Finding Orphaned Groups - awickham.com" 
date:   2018-03-08T15:27:31.616Z 
categories: powershell dbatools activedirectory
link: http://awickham.com/management/finding-orphaned-groups/ 
tags:
  - links
ogtype: article 
---

## Finding Orphaned Groups
 2 minute read
Finding Orphaned Groups
Active Directory groups are one of the easiest ways to allow your organization to have a separation of duties between Database Administrators and Identity and Access Management professionals. You can create an Active Directory group, create a login on the server, create a user in the database mapped to the login, and grant access to the user (which is actually a group). Then whenever people need to have access granted or revoked the Identity and Access Management professionals can handle that by just adding the actual users to the group.

The one obvious downfall to this setup is the additional management when setting up new databases or decommissioning old ones. Remembering to decommission old groups after I decommission a database is an area I struggle with. Sounds like a perfect solution for a script!