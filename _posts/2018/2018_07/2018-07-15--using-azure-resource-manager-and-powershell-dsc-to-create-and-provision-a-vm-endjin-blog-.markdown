---
layout: post 
title:  "	Using Azure Resource Manager and PowerShell DSC to create and provision a VM | endjin blog	" 
date:   2018-07-15T10:21:39.389Z 
categories: azurerm powershell psdsc
link: https://blogs.endjin.com/2015/07/using-azure-resource-manager-and-powershell-dsc-to-create-and-provision-a-vm/ 
tags:
  - links
ogtype: article 
---

> Using Azure Resource Manager and PowerShell DSC to create and provision a VM
July 29, 2015 by Richard Kerslake


Previously each component in Azure was deployed, managed, billed and monitored separately. Azure Resource Manager (ARM) is a new approach that allows you to declaratively state what a group of Azure infrastructure should look like as a template, then deploy that template in an idempotent way (i.e. you can run it multiple times and it will add any missing resources and just leave the rest in place). That resource group can then be managed, billed and monitored as a single unit. You’ll need to use the preview version of the management portal to see resource groups and the resources deployed using ARM.