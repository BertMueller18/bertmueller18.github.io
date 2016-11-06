---
layout: post 
published: true 
title: "Azure S2S VPN with RRAS - Deploy Azure" 
date: 2016-10-04T19:06:48.831Z 
link: http://www.deployazure.com/network/vpn/azure-s2s-vpn-rras/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Azure S2S VPN with RRAS
 November 14, 2015  Michael Roger

For a while I have wanted to connect my home lab up to my Azure subscriptions via site-to-site Azure S2S VPN. There are a few blogs online on how to do this in ASM, although I wanted to do this with Azure Resource Manager.

My current setup is a Hyper-V host with a Windows Server 2012 R2 guest VM that is behind a router that is capable of IPsec passthrough. Officially Microsoft do not support this behind NAT, but this just for testing purposes, so don’t use this in production environments!

Here are the steps that I used to connect my home network to ARM Azure S2S VPN.