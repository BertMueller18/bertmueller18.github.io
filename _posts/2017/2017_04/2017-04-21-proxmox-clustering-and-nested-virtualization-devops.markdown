---
layout: post 
title:  "Proxmox clustering and nested virtualization - DevOps" 
date:   2017-04-20T23:24:21.491Z 
categories: proxmox cluster linux
link: https://icicimov.github.io/blog/virtualization/Proxmox-clustering-and-nested-virtualization/ 
tags:
  - links
ogtype: article 
---

> Proxmox clustering and nested virtualization

 12 minute read ,  Sep 16, 2016
The motivation for creating this setup is the possibility of having Encompass private virtualization cloud deployed in any third party infrastructure provider DC, like for example SoftLayer that we already use to host our product on Bare-Metal serves. The solution is based on Proxmox PVE (Proxmox Virtualization Environment) version 4.1.x (upgraded to 4.2 later) with KVM as hypervisor. As stated on their website, Proxmox VE is a powerful and lightweight open source server virtualization software, optimized for performance and usability. For maximum flexibility, Proxmox VE supports two virtualization technologies - Kernel-based Virtual Machine (KVM) and container-based virtualization with Linux Containers (LXC).