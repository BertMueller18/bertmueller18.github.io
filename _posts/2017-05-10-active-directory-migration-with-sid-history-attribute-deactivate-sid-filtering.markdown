---
layout: post 
title:  "Active Directory Migration with SID-History attribute: Deactivate SID filtering" 
date:   2017-05-10T15:37:24.327Z 
categories: admt sidhistory activedirectory
link: http://activedirectoryfaq.com/2013/11/sid-history-deactivate-sid-filtering-to-migrate-user-accounts/ 
tags:
  - links
ogtype: article 
---

## SID-History: Deactivate SID filtering to migrate user accounts

For the purpose of an Active Directory Migration first one or more domains are created parallel to the existing Active Directory structure. After the establishment of the target environment user and group accounts are migrated to the new environment. Usually, migration tools are used for setting the SID history attribute for this purpose. Through the SID (security identifier) of each object the user permissions are assigned. The attribute SID-History contains the old SIDs of the source account. This way the user is assigned identical permissions to resources as he had in the source environment before the migration.

To use the attribute SID-History , SID filtering must be deactivated in the resource domain.


Typically, SID filtering is activated for security reasons and should be reactivated after the migration.

SID filtering deactivation in a domain:

Resource-Domain: Domain where the resource server are located

Account-Domain: Domain where the user accounts are located which need to access the resources


1
netdom trust <em>Resource-Domain</em> /domain:<em>Account-Domain</em> /quarantine:<em>No </em>

1
(Run the command as Administrator in the source domain)
Error message “Access denied”:

Add the administrator account of the account domain in the administrators group of the resource domain
Log in at the DC of the account domain with the administrator account
Call the command