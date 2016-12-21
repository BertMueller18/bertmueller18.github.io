---
layout: post 
published: true 
title: "Export Azure Resource Groups to ARM Templates with PowerShell – Build Azure" 
date: 2016-07-10T21:23:20.683Z
categories: azure azurerm powershell
link: https://buildazure.com/2016/03/30/export-azure-resource-groups-to-arm-templates-with-powershell/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Export Azure Resource Groups to ARM Templates with PowerShell
The latest release of Azure PowerShell includes the new “Export-AzureRMResourceGroup” cmdlet. This cmdlet allows you to specify the name of a Resource Group and it will export the resources for that group into an ARM Template json file. This new cmdlet is part of the new Azure PowerShell release that was just released today!

Export-AzureRMResourceGroup -ResourceGroupName “MyResourceGroup”

When run, this cmdlet will export the full configurations of the specified Azure Resource Group to a json file. Combining this capability along with the Azure QuickStart Templates and you should have everything you need to start automating all your Azure Resource deployments with ARM Templates!