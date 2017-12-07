---
layout: post 
title:  "Deploy a SharePoint 2016 Standalone VM in Azure using PowerShell Desired State Configuration (DSC) – Crawl, Walk, Run, Automate" 
date:   2017-12-07T07:54:39.055Z 
categories: azure powershell psdsc automation
link: http://nikcharlebois.com/deploy-a-sharepoint-2016-standalone-vm-in-azure-using-powershell-desired-state-configuration-dsc/ 
tags:
  - links
ogtype: article 
---

> Deploy a SharePoint 2016 Standalone VM in Azure using PowerShell Desired State Configuration (DSC)
 2017-04-06  Nik Charlebois	 Tutorial  556 8 Comments
In the PowerShell Desired State Configuration (DSC) world, you really have two options when it comes down to configuring a machine. You can either use Push mode to manually “push” a DSC script into a machine’s Local Configuration Manager (LCM) memory, or use a Pull Server and connect your machine to it and let them obtain their DSC script themselves. In the Azure world, we have something called “Azure Automation DSC” which is effectively a PowerShell Desired State Configuration Pull Server in the cloud, managed as “Software-as-a-Service” (SaaS). With Azure Automation DSC, you can manage both on-premises and Azure VMs by having them connect back to your Azure Automation Account as if it was just a regular DSC Pull Server.