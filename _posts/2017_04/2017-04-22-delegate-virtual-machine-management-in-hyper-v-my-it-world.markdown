---
layout: post 
title:  "Delegate Virtual Machine Management in Hyper-V – My IT World" 
date:   2017-04-22T08:48:42.468Z 
categories: hyper-v
tags:
  - links
ogtype: article 
---

> DELEGATE VIRTUAL MACHINE MANAGEMENT IN HYPER-V

 February 14, 2016  Arthur REMY Comments  1 Comment
TwitterLinkedInFacebookGoogle+
The most simple and effective method of enabling others to manage Hyper-V and virtual machines is to add them to the Hyper-V Administrators local security group for each of the Hyper-V hosts to which you plan to delegate management. However, this might not be the most secure method because doing so gives the new administrators permissions to change virtual switch and host settings in addition to VMs.

To delegate access to individual VMs, you need to modify the Hyper-V Authorization Manager store. This enables you to create task and role definitions to which you can delegate access. Find below the general steps to modifying the Hyper-V services authorization.

In order to accomplish this, launch an MMC (Microsoft Management Console) session, and add the Authorization Manager to the console.