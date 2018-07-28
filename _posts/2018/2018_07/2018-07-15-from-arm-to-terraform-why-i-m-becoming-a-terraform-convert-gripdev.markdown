---
layout: post 
title:  "From ARM to Terraform: Why I’m becoming a Terraform convert | GripDev" 
date:   2018-07-15T10:08:24.479Z 
categories: terraform azure azurerm
link: https://blog.gripdev.xyz/2018/06/21/from-arm-to-terraform-why-im-becoming-a-terraform-convert/ 
tags:
  - links
ogtype: article 
---

## From ARM to Terraform: Why I’m becoming a Terraform convert
JUNE 21, 2018
LAWRENCEGRIPPER
#ARM, #TERRAFORM, AZURE
LEAVE A COMMENT
Let me give you some background: I’ve been a heavy user of the Azure Resource Manager (ARM) templates for some time now. We’ve had some good times together. We’ve also had some bad times and boy have we seriously fallen out at times!

I’ve used ARM extensively to automate deployment, configuration and update of the infrastructure in Azure. I’ve used it on everything from single-person projects to large scale dual-region deployments of services with critical live traffic.

The takeaway for me has been: ARM is solid, reliable and does what I need – however, it isn’t always the easiest to use and it forces a wall between infrastructure deployment and application configuration which I’ve always found to be painful.

For example, when working with Azure Storage through ARM you can create a storage account, but you can’t create ‘queues’ or upload ‘blobs’ into the account. Another example – you can create an Azure Kubernetes cluster with AKS but you