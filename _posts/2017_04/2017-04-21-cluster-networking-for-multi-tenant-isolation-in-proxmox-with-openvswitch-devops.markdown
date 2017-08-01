---
layout: post 
title:  "Cluster Networking for Multi-tenant isolation in Proxmox with OpenVSwitch - DevOps" 
date:   2017-04-20T23:35:32.749Z 
categories: proxmox networking openvswitch vxlan gre
link: https://icicimov.github.io/blog/virtualization/Cluster-Networking-for-Multi-tenant-isolation-in-Proxmox-with-OpenVSwitch/ 
tags:
  - links
ogtype: article 
---

> Cluster Networking for Multi-tenant isolation in Proxmox with OpenVSwitch

 15 minute read ,  Sep 22, 2016
This is probably the most complex part of the setup. It involves network configuration of the cluster in a way that the instances running on different nodes can still talk to each other. This is needed in order to provide clustering and HA of the VM services them self.