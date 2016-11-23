---
layout: post 
title:  "KEMP Series: How to Restrict Exchange Admin Center Access From the Internet Using KEMP VLB | The EXPTA {blog}" 
date:   2016-11-23T22:50:24.437Z 
categories: loadbalancer exchange exchange2013 exchange2016
link: http://www.expta.com/2015/02/kemp-series-how-to-restrict-exchange.html 
tags:
  - links
ogtype: article 
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

The EAC is part of the ECP virtual directory and is the same virtual directory used in OWA to manage user settings, such as Out of Office settings. If you were to disable or not publish the entire ECP virtual directory to the Internet in order to block EAC access, it would prevent external users from accessing many settings from OWA.
Update: Microsoft just released a new article, Configuring Multiple OWA/ECP Virtual Directories on the Exchange 2013 Client Access Server Role, which describes how to create a separate vDir for the Exchange Admin Center. If you chose the Microsoft solution to disable Internet access to EAC (and I do, if you want Microsoft support) know that you need to follow those step EXACTLY and you will need to redo that setup after every CU. If you wish to load balance the new vDir you will also need to create new SubVSs on the KEMP LoadMaster.
Let's get started configuring EAC restrictions on the KEMP LoadMaster. Log into the LoadMaster with the bal account and navigate to Rules & Checking > Content Rules.