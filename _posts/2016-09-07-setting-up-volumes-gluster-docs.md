---
layout: post 
published: true 
title: "Setting Up Volumes - Gluster Docs" 
date: 2016-09-07T05:33:27.479Z 
link: https://gluster.readthedocs.io/en/latest/Administrator%20Guide/Setting%20Up%20Volumes/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Setting up GlusterFS Server Volumes

A volume is a logical collection of bricks where each brick is an export directory on a server in the trusted storage pool. Most of the gluster management operations are performed on the volume.

To create a new volume in your storage environment, specify the bricks that comprise the volume. After you have created a new volume, you must start it before attempting to mount it.