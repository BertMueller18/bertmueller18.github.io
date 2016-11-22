---
layout: post 
title:  "Building distributed mesh networks of LXC containers        " 
date:   2016-11-22T22:33:29.728Z 
categories: sdn tinc linux
link: https://www.flockport.com/building-distributed-mesh-networks-of-lxc-containers/ 
tags:
  - links
ogtype: article 
---

> Building distributed mesh networks of LXC containers

This is unique as we are going to connect 2 (or more) containers behind a NAT network with Tinc. With this config we try not to touch the host networking layer too much. This is a mesh network enabled in containers networking space and the only setting on the host is a single port forward of tcp/udp 655 on one of the hosts, to a container. In this scenario containers will have 2 IPs, the containers basic lxcbr0 NAT network and the Tinc vpn network