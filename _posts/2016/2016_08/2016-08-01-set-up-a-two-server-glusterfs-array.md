---
layout: post 
published: true 
title: "Set up a two-server GlusterFS array" 
date: 2016-08-01T20:07:22.855Z
categories: linux gluster storage
link: https://support.rackspace.com/how-to/set-up-a-two-server-glusterfs-array/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Set up a two-server GlusterFS array
Last updated on: 2016-01-12 Authored by: Matt Sherborne
This article presents a step-by-step description for how to set up a two-server GlusterFS array.

Having two web servers behind a load balancer means that they have to synchronize the files that they serve and write to. On modern Linux distributions, GlusterFS is the easiest way to accomplish this task. The examples in this article use Ubuntu Trusty as the Linux distribution. This article is the first in a series of three articles about using GlusterFS within the Rackspace cloud environment.