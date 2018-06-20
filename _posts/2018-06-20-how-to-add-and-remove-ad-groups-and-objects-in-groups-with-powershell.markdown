---
layout: post 
title:  "How to Add and Remove AD Groups and Objects in Groups with PowerShell" 
date:   2018-06-20T20:59:14.901Z 
categories: activedirectory powershell
link: https://blog.netwrix.com/2018/06/19/how-to-add-and-remove-ad-groups-and-objects-in-groups-with-powershell/?rid=gDd88kwH 
tags:
  - links
ogtype: article 
---

> How to Add and Remove AD Groups and Objects in Groups with PowerShell
  
Jeff Melnick

Published: June 19, 2018

Microsoft Active Directory serves as a centralized point for the administration, authorization and authentication. In AD, access to network resources is granted to security principals, such as user accounts and computer accounts, and those permissions can change over time. To simplify access management and improve security, medium and large companies often use Active Directory security groups, which can contain user accounts, computer accounts and other groups. They often also use distribution groups to manage email distribution lists. Both security and distribution groups have unique security identifiers (SIDs) and globally unique identifiers (GUIDs).

The ADUC MMC snap-in is great for managing both types of groups, but PowerShell is a much more efficient way to manage them in bulk.