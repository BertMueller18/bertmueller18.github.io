---
layout: post
title:  "Options for Migrating Azure VMs from ASM (v1) to ARM (v2)"
date:   2017-01-11T17:03:59.455Z
categories: azure azurerm powershell migration
tags:
  - links
ogtype: article
---

## Options for Migrating Azure VMs from ASM (v1) to ARM (v2)

31 May 2016  4 Comments  Posted in Azure, devops, Automation


Today, the Azure portal allows you to create 2 types of VMs. These types refer mainly to the platform atop which your VMs run. Before I continue with this post, it may be handy establishing what the terminology means:

CLASSIC/ASM

Classic or v1 VMs run on top of the older Azure Service Management (ASM) technology. ASM infrastructures can be managed through both the old and the new portals and Azure PowerShell/CLI. However, some of the v1 features are not yet, and may never be, available on the new Azure Portal.

NEW/ARM

Resource Manager or v2 VMs run on top of the new Azure Resource Management (ARM) technology. V2 infrastructure is only available through the new portal and offers significant benefits over its predecessor, mainly in the automation and DevOps domain. ARM templates allow you to export/import your infrastructure and enable high degrees of automation.

Creating new resources on Azure should be done against the v2 infrastructure. However, today, there are plenty of customers that still run their existing VMs on the “old”, ASM platform. This post will explain the 4 options for migrating v1 VMs to v2.
