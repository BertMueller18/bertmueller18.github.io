---
layout: post 
title:  "Setting up a Share Using Windows ACLs - SambaWiki" 
date:   2018-09-20T14:15:38.755Z 
categories: samba activedirectory security
link: https://wiki.samba.org/index.php/Setting_up_a_Share_Using_Windows_ACLs#Enable_extended_ACL_support_in_smb.conf 
tags:
  - links
ogtype: article 
---

## Setting up a Share Using Windows ACLs


Extended access control lists (ACL) enable you to set permissions on shares, files, and directories using Windows ACLs and applications. Samba supports shares using extended ACLs on:

Domain members
Active Directory (AD) domain controllers (DC)
NT4 primary domain controller (PDC)
NT4 backup domain controllers (BDC)
Standalone hosts
As an alternative to extended ACLs, you can set up shares using POSIX ACLs. For details, see Setting up a Share Using POSIX ACLs.

	Samba does not support using POSIX ACLs on a DC. You must use Windows ACLs.