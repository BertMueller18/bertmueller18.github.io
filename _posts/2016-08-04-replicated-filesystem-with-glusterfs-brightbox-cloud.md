---
layout: post 
published: true 
title: "Replicated filesystem with GlusterFS - Brightbox Cloud" 
date: 2016-08-04T17:08:19.204Z 
link: https://www.brightbox.com/docs/guides/glusterfs/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Replicated filesystem with GlusterFS

GlusterFS is a scalable and highly available network filesystem that’s pretty easy to get up and running.

This guide will take you through building a shared filesystem with GlusterFS that is replicated across our two UK datacentres. Files written by any cloud server in the cluster can be read by any other server instantaneously, and those files will still be accessible even if a server, or an entire datacentre becomes unavailable.