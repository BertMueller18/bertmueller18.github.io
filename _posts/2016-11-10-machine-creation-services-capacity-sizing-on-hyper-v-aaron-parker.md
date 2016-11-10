---
layout: post 
published: true 
title: "Machine Creation Services Capacity Sizing on Hyper-V - Aaron Parker" 
date: 2016-11-10T20:37:00.149Z 
link: http://stealthpuppy.com/mcs-capacity-sizing-hyper-v/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Machine Creation Services Capacity Sizing on Hyper-V


Contents [show]
To understand sizing Machine Creation Services on Hyper-V, we should first look at how XenDesktop creates virtual machines across the various deployment choices. XenDesktop 7.9 and 7.11 have introduced new features to MCS that will require additional consideration for storage requirements over previous versions.

In this article, I’ll cover the deployment options at a high level, including:

Delta Clones – this has been the traditional deployment approach for MCS, where virtual machines reference a base image and store changes in a delta disk. In Hyper-V parlance, this is referred to as a differencing disk. Delta clones work for XenApp, pooled and dedicated clone VMs
Delta Clones with Storage Optimisation – this is the new default option for MCS deployments since XenDesktop 7.9. IO optimisation enables a cache in RAM with overflow to disk
Full Clones – new in XenDesktop 7.11 is the ability to deploy full clones from a master image and rely on the storage platform to provide optimisation