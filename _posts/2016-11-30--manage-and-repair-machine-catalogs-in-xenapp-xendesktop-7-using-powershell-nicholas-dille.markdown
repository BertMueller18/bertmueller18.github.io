---
layout: post 
title:  "    Manage and Repair Machine Catalogs in #XenApp/#XenDesktop 7 using #PowerShell · Nicholas Dille" 
date:   2016-11-29T23:42:23.850Z 
categories: citrix xendesktop powershell
link: http://dille.name/blog/2015/01/28/manage-and-repair-machine-catalogs-in-xenappxendesktop-7-using-powershell/ 
tags:
  - links
ogtype: article 
---

> Manage and Repair Machine Catalogs in #XenApp/#XenDesktop 7 using #PowerShell
Published on 28 Jan 2015
Tags #MCS#PowerShell#XenApp#XenDesktop
If you are using Machine Creation Services (MCS) extensively, you strongly depend on the hosting infrastructure. But sometimes it becomes necessary to reorganize the structure inside the hosting infrastructure. In my case, a customer needed to rename clusters, datastores and virtual networks inside VMware vCenter. Unfortunately, machine catalogs cannot be reconfigured to accomodate for those changes. The only way to repair machine catalogs is to recreate them. That’s why I have created the following PowerShell cmdlets.