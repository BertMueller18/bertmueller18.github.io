---
layout: post 
title:  "Setup Azure VPN using PowerShell - Powershellbros.com" 
date:   2018-06-20T21:22:25.627Z 
categories: azure azurerm powershell vpn
link: http://www.powershellbros.com/setup-azure-vpn-using-powershell/ 
tags:
  - links
ogtype: article 
---

> Setup Azure VPN using PowerShell
Posted on June 20, 2018 by Artur Brodziński

Hey Scripters! Today I want to share with you my script for setup Azure VPN using PowerShell.

In few words, script is using basic Azure module command.
At the begginig you should have your VPN device already configured and once it is done, you can start configuration from Azure site.
To configure VPN device you should already have public IP created in Azure.
All variables depends on your on premise environment configuration. You should know for example, which VNET will be used in Azure.