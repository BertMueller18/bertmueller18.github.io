---
layout: post 
published: true 
title: "Creating a custom Virtual Machine for deployment on Azure – Microsoft Faculty Connection" 
date: 2016-10-12T20:35:23.275Z 
link: https://blogs.msdn.microsoft.com/uk_faculty_connection/2016/09/22/creating-a-custom-virtual-machine-for-deployment-on-azure/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Creating a custom Virtual Machine for deployment on Azure
★★★★★★★★★★★★★★★
Lee StottSeptember 22, 20160
0
14
0
 

I was speaking at a University this week where they wanted to deploy specific Linux machine for their labs based on specific build of Red Hat Linux. the University already had a custom build for their labs PC but wanted to make this available as an Azure VM. 

The team already had PCs on campus which had the base image.  The following is a short guide on using  Azure ARM CLI. and taking an existing image to Azure a comprehensive guide is available at https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-linux-cli-deploy-templates/