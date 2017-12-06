---
layout: post 
title:  "itToby: Tunnel to the Cloud: pfSense to Azure Site to Site IPsec Connection" 
date:   2017-12-06T22:23:25.356Z 
categories: pfsense azure vpn ipsec
link: http://blog.ittoby.com/2016/10/tunnel-to-cloud-pfsense-to-azure-site.html 
tags:
  - links
ogtype: article 
---

> itToby
Because if I don't write it down I might forget it.

Thursday, October 27, 2016
Tunnel to the Cloud: pfSense to Azure Site to Site IPsec Connection
Do you have multi-continent datacenters with gobs of bandwidth, IOps, and processing capability? No? I can help get you part of the way there... a network presence in one. 


A tunnel.
A Site to Site Connection?

It's easier to think of this as an extension to your network into another datacenter over the internet. Using IPsec we can provide a relatively (comments at the end) secure, direct connection between on on-premises datacenter and Azure hosted resources by encrypting the traffic that flows between the two.  What do I mean by: 
Secure: IPsec tunnels all your traffic so it is encrypted over the internet; in reality, this is really "more secure" rather than definitively secure, as the effective security depends highly on implementation specifics.
Direct: Your router (played by pfSense in this case) will recognize the Azure site as another routable network within the boundaries of your own, enabling you to talk to Azure resources as if they were in your own datacenter.
Note: this works for Amazon Web Services (AWS) as well but is slightly more complex. Fortunately pfSense includes a wizard that works, but takes a lot of the fun out of it as it strips you of understanding how it works. In addition the wizard is necessary because of how Amazon does VPC routing, whereas Azure is a bit more straightforward.

This article will also be useful for non-pfSense devices since we discuss the details of the IPsec tunnel; the information here should be applicable to any IPsec solution.

With that, let's get to it!