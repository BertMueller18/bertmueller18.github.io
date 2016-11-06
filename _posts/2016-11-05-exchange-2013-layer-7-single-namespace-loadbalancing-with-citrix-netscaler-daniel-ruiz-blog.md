---
layout: post 
published: true 
title: "Exchange 2013 Layer 7 single namespace loadbalancing with Citrix NetScaler | Daniel Ruiz - Blog" 
date: 2016-11-05T22:31:30.107Z 
link: https://danielruiz.net/2015/05/26/exchange-2013-layer-7-single-namespace-loadbalancing-with-citrix-netscaler/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Exchange 2013 Layer 7 single namespace loadbalancing with Citrix NetScaler

MAY 26, 2015 28 COMMENTS
** Updated with custom Ciphers, SSLv3 disabled on Content Switch and LBs, and SSL certificate bindings to the vServers***
I recently had to engage on a very complex deployment, where one of the goals was to utilize the Citrix NetScaler for Exchange 2013 services for a single namespace with Layer 7 and no session affinity.
In this scenario, a single namespace is deployed for all the HTTP protocol clients (mail.yourdomain.com). The load balancer is configured to utilize Layer 7, meaning SSL termination occurs and the load balancer and it knows about the target URLs. The NetScaler is also configured to check the health of the target services in the load balancing pool which requires a health probe to be configured on each Exchange virtual directory.
With this, as long as the health probes response is healthy, the NetScaler will keep the traffic in the load balancing pool. However, if lets say OWA health probe fails for any reason, the NetScaler will remove the target server(s) from the load balancing pool for future requests.
The key to this deployment is to set up Content Switching which enables the NetScaler appliance to direct requests sent to the same Web host to different servers with different content. For example, you can configure the appliance to direct requests for dynamic content (such as URLs with a suffix of .asp, .dll, or .exe) to one server and requests for static content to another server. You can configure the appliance to perform content switching based on TCP/IP headers and payload.