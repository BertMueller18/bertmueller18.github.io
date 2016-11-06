---
layout: post 
published: true 
title: "Step-By-Step: Deploying a Domain Joined Nano Server via PowerShell | CANITPRO" 
date: 2016-05-08T14:56:17.021Z 
link: https://blogs.technet.microsoft.com/canitpro/2016/04/20/step-by-step-deploying-a-domain-joined-nano-server-via-powershell/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Recently I’ve put together a PowerShell module called DeployImage with the intent to simplify the deployment of a WindowsIMage file.  In this case, my goal was to make NanoServer an easily deployable option for the average system administrator.  So began my experimentation with Windows Server 2016 to get a fully deployed Nano server online.

Deploying Nano Server is no different than deploying any other WIM file except for the fact that you must compensate for is it is headless environment.

This requires a plan to have certain tasks completed within the server without actually touching it.   These tasks include:

Assigning a Static IP address
Naming the workstation
Joining it to a Domain
