---
layout: post
title:  "Installing Azure PowerShell on Server 2012 R2 using PowerShell :: Ned in the Cloud"
date:   2017-01-07T23:12:03.702Z
categories: azure powershell deployment
link: https://nedinthecloud.com/2017/01/07/installing-azure-powershell-on-server-2012-r2-using-powershell/
tags:
  - links
ogtype: article
---

## Installing Azure PowerShell on Server 2012 R2 using PowerShell

Currently I am working on a project to create a CICD pipeline in Azure Stack.  I am planning to use Team Foundation Server 2015, running on a virtual machine on Azure Stack.  I want the installation of TFS to be automated using ARM templates and a CustomScript extension.  (I would use DSC, but I feel I’ve shaved the yak enough already).  The installer and configuration files are sitting in Azure Blob storage, and I want to be able to pull them from the Server 2012 R2 instance that will be running TFS.  I can do it using Invoke-WebRequest or Start-BitsTransfer, but I wanted to try using the Azure PowerShell storage cmdlets instead.  Of course the vanilla install of Server 2012 R2 does not have the Azure modules or PowerShellGet module to access the PowerShell Gallery and install them.  So instead I am going to use Invoke-WebRequest and Github to grab it instead.
