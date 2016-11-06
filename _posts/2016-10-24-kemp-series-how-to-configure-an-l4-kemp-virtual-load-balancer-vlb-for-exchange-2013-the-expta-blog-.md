---
layout: post 
published: true 
title: "KEMP Series: How to Configure an L4 KEMP Virtual Load Balancer (VLB) for Exchange 2013 | The EXPTA {blog}" 
date: 2016-10-24T20:38:02.526Z 
link: http://www.expta.com/2015/02/kemp-series-how-to-configure-l4-kemp.html 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> KEMP Series: How to Configure an L4 KEMP Virtual Load Balancer (VLB) for Exchange 2013
Saturday, February 7, 2015
This is part four in a series of articles detailing load balancing for Exchange using the KEMP virtual load balancer (VLB). In this article we will be configuring the VLB as a Layer 4 load balancer for Exchange 2013.

The other articles in this series are:
Introduction to Load Balancing for Exchange and Other Workloads
How to Configure General Settings on the KEMP Virtual LoadMaster
How to Configure an L7 KEMP Virtual Load Balancer (VLB) for Exchange 2013
How to Configure an L4 KEMP Virtual Load Balancer (VLB) for Exchange 2013 (this article)
How to Restrict Exchange Admin Center Access From the Internet Using KEMP VLB
My first article explains the basics of load balancing and how to download a free copy of KEMP Virtual Load Master for your home lab. As a refresher, here's a brief explanation of the differences between Layer 7 and Layer 4 load balancing.
Layer 7 Load Balancing
L7 load balancing happens at the application layer. Health checks are performed on the applications (for example OWA, EWS, ActiveSync, etc.). The SSL connection must terminate on the load balancer, the content is inspected, and then re-encrypted back to the real servers. This requires that the L7 load balancer has to have an understanding of the applications being load balanced. It also usually involves some sort of persistence, such as cookie-based or source IP. Because of all this, L7 load balancing is more complex. Exchange 2010 required L7 load balancing due to the different ways that each application protocol handled persistence. Exchange 2013 does not require persistence even when using L7 load balancing.

Layer 4 Load Balancing
L4 load balancing happens at the network layer after routing is compete (Routing occurs at Layer 3). Health checks are performed on the servers, not the applications. Layer 4 load balancers do not decrypt, inspect, and re-encrypt SSL traffic. This means L4 load balancers have higher performance and are less complex, but the load balanced application must support it. Exchange 2013 CAS is designed for L4 load balancing, but also supports L7 load balancing.