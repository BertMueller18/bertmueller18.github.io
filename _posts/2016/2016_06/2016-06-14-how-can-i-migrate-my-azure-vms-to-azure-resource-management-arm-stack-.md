:---
layout: post 
published: true 
title: "How can I migrate my Azure VMs to Azure Resource Management (ARM) stack?" 
date: 2016-06-14T12:25:27.952Z 
categories: azure devops automation azurerm
link: https://cmatskas.com/migrate-your-azure-vms-to-azure-resource-management-arm-stack/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## How can I migrate my Azure VMs to Azure Resource Management (ARM) stack?

06 April 2016  

That's a perfectly good question and one that many teams are facing lately. There is a valid reason to want to upgrade. The Azure Resource Manager (ARM) has a lot of advantages over it's predecessor. The biggest one is automation. ARM templates allow you to easily capture, configure and deploy resources and resource groups on Azure using PoSH (PowerShell) and simple Json files. This is great for DevOps! If you're starting with Azure now, then ARM makes absolute sense and is the default option. However, there are many companies that are stuck in v1 i.e the Azure Service Management (ASM) stack waiting for a reliable way to upgrade.

In this post, we will take advantage of a new Open Source tool, conveniently named ASM2ARM to migrate a single VM from the v1/ASM stack to the v2/ARM stack.