---
layout: post 
title:  "Adding GlusterFS shared storage to Proxmox to support Live Migration - DevOps" 
date:   2017-04-20T23:19:00.392Z 
categories: proxmox gluster linux
link: https://icicimov.github.io/blog/virtualization/Adding-GlusterFS-shared-storage-to-Proxmox-to-support-Live-Migration/ 
tags:
  - links
ogtype: article 
---

> Adding GlusterFS shared storage to Proxmox to support Live Migration

 4 minute read ,  Sep 17, 2016
To be able to move VM’s from one cluster member to another their root, and in fact any other attached disk, needs to be created on a shared storage. PVE has built in support for the native GlusterFS client among the other storage types which include LVM, NFS, iSCSI, RBD, ZFS and ZFS over iSCSI.