---
layout: post 
title:  "Deploy Windows Admin Center in HA through Kemp Load Balancer -" 
date:   2018-05-04T13:44:39.734Z 
categories: windows admincenter activedirectory kemp loadbalancer powershell
link: https://www.tech-coffee.net/deploy-windows-admin-center-in-ha-through-kemp-load-balancer/ 
tags:
  - links
ogtype: article 
---

> Deploy Windows Admin Center in HA through Kemp Load Balancer
Posted by: Romain Serre  in Windows Admin Center May 3, 2018	0 67 Views

Windows Admin Center (formerly Honolulu Project) was released in April 2018 by Microsoft. WAC is a web-based management tool to help to administrate Windows Server and hyperconverged cluster. In part of my job, I use primarily Windows Admin Center for Storage Spaces Direct Cluster and to manage Windows Server in Core edition especially drivers. Since the release of Windows Admin Center, Microsoft provides the capability to deploy it in high availability. In this topic we’ll see how to deploy Windows Admin Center in this manner. Moreover, some of customers want to connect to WAC through a load balancer such as Kemp to avoid private certificate management and to be able to connect from the Internet. So, we’ll see also how to connect to WAC through a Kemp load balancer.