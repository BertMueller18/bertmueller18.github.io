---
layout: post 
published: true 
title: "Create Azure Resource Manager virtual machines by using PowerShell – Part 1 | Hey, Scripting Guy! Blog" date: 2016-06-21T07:14:27.154Z 
categories: azure azurerm powershell
link: https://blogs.technet.microsoft.com/heyscriptingguy/2016/06/06/create-azure-resource-manager-virtual-machines-by-using-powershell-part-1/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Summary: Use PowerShell cmdlets to start to create a virtual machine in Azure Resource Manager.

 How do I create virtual machines (VMs) in Azure Resource Manager by using PowerShell? Where do I start?

 Honorary Scripting Guy, Sean Kearney, is here, and we’re going to give you some basic step-by-step guidance this week about how to spin up a VM with Azure Resource Manager PowerShell cmdlets. We’re also going to reference back to some cool tricks that we picked up last week to obtain data from a previous VM so that you don’t have to go about digging for the settings.

When I go to prepare a VM in Azure Resource Manager (outside of the actual preparation of the infrastructure such as our network or resource groups), I tend to think of six key tasks:

Set up the base configuration (VM size and name)
Set up the storage for the operating system image
Define the network configuration (virtual network, card, subnet, security group)
Set up the operating-specific details (template for the image)
Assign the user ID and password for the operating system
Spin up the VM