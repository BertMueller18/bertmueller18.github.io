---
layout: post
published: true
title: "KEMP Series: How to Restrict Exchange Admin Center Access From the Internet Using KEMP VLB | The EXPTA {blog}"
date: 2016-10-24T20:40:31.792Z
categories: kemp exchange exchange2013 
link: http://www.expta.com/2015/02/kemp-series-how-to-restrict-exchange.html
tags:
  - links
ogtype: article
bodyclass: post
---

> KEMP Series: How to Restrict Exchange Admin Center Access From the Internet Using KEMP VLB
Tuesday, February 10, 2015
This is part five in a series of articles detailing load balancing for Exchange using the KEMP virtual load balancer (VLB). In this article I will explain how to restrict Exchange Admin Center (EAC) access from the Internet using KEMP LoadMaster.

The other articles in this series are:
Introduction to Load Balancing for Exchange and Other Workloads
How to Configure General Settings on the KEMP Virtual LoadMaster
How to Configure an L7 KEMP Virtual Load Balancer (VLB) for Exchange 2013
How to Configure an L4 KEMP Virtual Load Balancer (VLB) for Exchange 2013
How to Restrict Exchange Admin Center Access From the Internet Using KEMP VLB (this article)
My first article explains the basics of load balancing and how to download a free copy of KEMP Virtual Load Master for your home lab. I'll assume you've already configured it for Layer 7 load balancing.
Note: Since the following procedures rely on SubVSs and traffic inspection, this configuration will only work with Layer 7 load balancing. Layer 4 load balancing cannot inspect traffic and therefore cannot be used to deny access to the EAC.
The Exchange Admin Center (EAC) is the web-based management console used to manage your Microsoft Exchange Server 2013 infrastructure. As such, some customers want to block EAC access from the Internet.
