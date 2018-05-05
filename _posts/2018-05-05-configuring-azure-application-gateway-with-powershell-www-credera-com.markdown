---
layout: post 
title:  "Configuring Azure Application Gateway With PowerShell - www.credera.com" 
date:   2018-05-05T19:09:01.443Z 
categories: azure powershell loadbalancer networking
link: https://www.credera.com/blog/technology-solutions/configuring-azure-application-gateway-with-powershell/ 
tags:
  - links
ogtype: article 
---

## Configuring Azure Application Gateway With PowerShell
 JW Walton November 17, 2017  No Comments
Microsoft Azure Application Gateway is a Layer 7 application delivery controller (ADC) offered as a service in Azure. It provides load balancing, SSL termination, end-to-end SSL, URL path-based routing, and basic web application firewall (WAF) functionality. In a previous blog post, I addressed the question “Is Azure Application Gateway a Good Fit for My Application?” This blog post assumes you’ve already decided an Azure Application Gateway is the way you want to go, but now you need to start configuring it. While you can use the Azure Portal to configure most elements of the Azure Application Gateway, to do some tasks you need to use PowerShell. And the good news is that once you understand how the Azure Application Gateway PowerShell works, it is much easier and faster than using the Portal to add configurations.