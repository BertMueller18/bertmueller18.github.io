---
layout: post 
title:  "Deploy VMware VMs with PowerCLI and MDT - WinSysBlog" 
date:   2017-10-02T09:48:56.151Z 
categories: powershell powercli mdt mdt2013 deployment
link: https://winsysblog.com/2017/09/deploy-vmware-vms-powercli-mdt.html 
tags:
  - links
ogtype: article 
---

## Deploy VMware VMs with PowerCLI and MDT
Published by Dan Franciscus on September 20, 2017

If you are managing Windows servers, chances are you have a mix of physical and virtual servers in your data center. While VMware provides a method to create VMs from templates to simplify server deployments, this method obviously does not work for deploying physical servers. Fortunately, you can use MDT to deploy a physical or virtual server, which provides one solution for configuring on-premises server deployment tasks.

For new servers to use MDT, they need to boot to Windows PE using the preboot execution environment (PXE). We most commonly do this with Windows Deployment Services (WDS) or by booting directly to CD/ISO Lite Touch media, which circumvents WDS. For deploying new VMs, I prefer to attach the Lite Touch ISO file to a VM. Using this method, I do not have to depend on PXE. In addition, I can automate creating a new VMware virtual machine by just running a PowerCLI cmdlet.

With my PowerCLI function New-MDTVM, you can easily deploy VMware virtual machines (VMs) with the Microsoft Deployment Toolkit (MDT).