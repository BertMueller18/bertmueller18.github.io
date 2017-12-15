---
layout: post 
title:  "My problem with optimizer tools - Logit Blog" 
date:   2017-11-26T22:11:35.824Z 
categories: windows10 citrix vmware vdi
link: http://www.logitblog.com/my-problem-with-optimizer-tools/ 
tags:
  - links
ogtype: article 
---

## My problem with optimizer tools

 November 26, 2017 Author: Ryan Bijkerk

Applying optimizations within a VDI environment is nowadays the de facto standard. There are different tools available to help you apply optimizations according to best practices. These optimizer tools are useful but also have a downside. In this blog post, I will share my problem with these optimizer tools.


The importance of optimizing
Before we start comparing different options it is import to understand the importance of optimizing a VDI environment. A default installation of an operating system contains roles and features which may not be used. These roles and features may look innocent but may consume resources in the background. This can result in a lower density of your VDI environment which increases the cost per desktop. Besides density, it may also affect overall user experience as applications become slower.

There are different components to optimize, like removing roles or features, disabling services and tasks or applying specific settings in the registry. But also think about antivirus solutions as they can heavily impact performance.

Collecting all these best practices is quite a search but luckily there are various tools available that contains these best practices.

Available optimizer tools: VMware vs Citrix

The two most common tools available today are VMware OSOT and Citrix Optimizer. Both are free and contains default templates for various operating systems. These tools provide a user interface which you can enable or disable specific optimizations.