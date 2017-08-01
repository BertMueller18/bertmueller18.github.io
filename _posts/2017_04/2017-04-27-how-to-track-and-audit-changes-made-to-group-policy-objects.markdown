---
layout: post 
title:  "How to Track and Audit Changes made to Group Policy Objects" 
date:   2017-04-27T14:39:40.041Z 
categories: activedirectory security 
link: https://www.lepide.com/how-to/audit-chnages-made-to-group-policy-objects.html 
tags:
  - links
ogtype: article 
---

## How to track and audit changes made to Group Policy Objects
In Microsoft Windows, Group Policy Object (GPO) controls the network by providing an integrated platform for the management and configuration of operating systems, applications and user settings in the Active Directory environment. Group Policy settings are stored in Group Policy Objects which can be associated with Sites, Domains and Organizational Units.

In large organizations, there can often be more than one administrator who takes care of the network through the Group Policy Management Console (GPMC). It’s important to audit Group Policy changes in order to determine the details of changes made to Group Policies by delegated users.

Group Policy Objects are stored at two different places: “Group Policy Template” and “Group Policy Container.” The Group Policy Templates are stored in the “%sysroot%\SYSVOL” folder. To monitor Group Policy changes, administrators must enable Group Policy change auditing and SYSVOL folder auditing. To monitor Group Policy changes completely, you must enable the auditing of DS Objects, Group Policy Container Objects and SYSVOL folder.