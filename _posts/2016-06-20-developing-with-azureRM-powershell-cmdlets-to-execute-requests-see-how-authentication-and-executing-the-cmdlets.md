---
layout: post 
published: true 
title: "Developing with Azure Resource Manager: PowerShell cmdlets | Learn how to use PowerShell to execute requests with the Azure Resource Manager. See how authentication and executing the cmdlets works.Zimmergren's thoughts on tech" 
date: 2016-06-20T21:51:43.006Z 
link: https://zimmergren.net/developing-with-azure-resource-manager-part-2-getting-started-with-the-azurerm-powershell-cmdlets/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Developing with Azure Resource Manager - Part 2 - Getting started with the AzureRm PowerShell cmdlets

In  Windows Azure Cloud azure resource manager By  Tobias Zimmergren

Part 0: Introduction to the article series
Part 1: Create an AzureRm Active Directory (AAD) Application using PowerShell
Part 2: Getting started with the AzureRm PowerShell cmdlets
Part 3: Build an application using C# which is using the Azure Resource Manager API's
Part 4: Tip: Azure Resource Explorer Tool
Part 5: Tip: Get all available api-version alternatives for the ARM endpoints
Part 6: Move Azure Resources from one Resource Group to another
Part 7: Download an Azure Publishing Profile (xml) programmatically using REST
Part 8: Programmatically export Resource Group template using the REST API
Part 9: Coming soon...
Introduction
This is the second part in my series about Azure Resource Manager. In this post we will take a look at some of the AzureRm PowerShell cmdlets to get us started. This article is assuming that you've already followed the steps as lined out in Part 1, to set up your AAD Application and Service Principals and saved your credentials etc.

Q: Why use a Service Principal rather than just a user/password from my normal account?

A: If you want automation from CI/a service or you want to have your custom applications authenticate to your AAD and work with Azure Resource Manager, you don't want to use your own username/password but instead a dedicated service user. This is why we have the Service Principal accounts dedicated for this.
