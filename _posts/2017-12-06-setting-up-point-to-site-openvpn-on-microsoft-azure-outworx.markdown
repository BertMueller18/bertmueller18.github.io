---
layout: post 
title:  "Setting up Point-to-Site OpenVPN on Microsoft Azure | OutworX" 
date:   2017-12-06T22:25:06.833Z 
categories: openvpn azure
link: http://www.outworx.com/blog/setting-up-point-to-site-openvpn-on-microsoft-azure/ 
tags:
  - links
ogtype: article 
---

> Setting up Point-to-Site OpenVPN on Microsoft Azure


Microsoft Azure has some nice paid services for creating site-to-site VPN.  Using these, you can create a hybrid cloud that connects your enterprise network to a Virtual Network on Azure.  But if you just want connect to a single Azure VM, this may be overkill.

This article discusses how to use OpenVPN to connect a Windows client on your local network to a Linux VM running in Azure.   We will be following the general outline found at the OpenVPN HOWTO.  Our Azure VM is running Ubuntu 14.04LTS.

Add OpenVPN to the Network ACL
Go the the Virtual Machines tab in the Azure portal.  Select the VM you want, and click on its Endpoints tab.  At the bottom of the screen, click on ‘+ ADD’ to add a new endpoint for OpenVPN.