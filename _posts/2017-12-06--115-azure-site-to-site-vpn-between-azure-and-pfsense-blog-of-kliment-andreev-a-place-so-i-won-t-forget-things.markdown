---
layout: post 
title:  "#115 Azure: Site-to-Site VPN between Azure and pfSense - Blog of Kliment Andreev - A place so I won't forget things" 
date:   2017-12-06T22:22:58.267Z 
categories: pfsense azure vpn ipsec
link: https://blog.iandreev.com/?p=3250 
tags:
  - links
ogtype: article 
---

> 
AZURE
#115 Azure: Site-to-Site VPN between Azure and pfSense
KLIMENT ANDREEV8TH OCT '170
 Post Views: 177
In this blog post I’ll describe how to create a VPN connection between an Azure subscription and a pfSense router with a public IP using dynamic routing. Before we proceed, you have to understand that the subnets can’t overlap in Azure and behind pfSense. So, if your home network is 192.168.1.0/24, you can’t have the same subnet in Azure. It is also a good practice to write down your subnets and subnet masks before hand, so there are no errors when creating the tunnel. Many times, the tunnel won’t work just because you are rushing things and not paying attention to the subnets and masks. So, here is my setup.
