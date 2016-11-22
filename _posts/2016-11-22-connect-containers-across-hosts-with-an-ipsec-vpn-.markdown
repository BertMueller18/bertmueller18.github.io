---
layout: post 
title:  "Connect Containers across Hosts with an IPSEC VPN        " 
date:   2016-11-22T22:34:10.588Z 
categories: sdn ipsec linux
link: https://www.flockport.com/connect-lxc-hosts-with-an-ipsec-vpn/ 
tags:
  - links
ogtype: article 
---

> Connect LXC hosts with an IPSEC VPN

We have covered connecting containers across several hosts previously with plain GRE tunnels and Tinc, which is an awesome little program to build secure mesh networks and VPNs. Today we are going to look at connecting containers across several LXC host with IPSEC. For most users I would recommend Tinc for ease of use, flexibility and performance however there may be some cases where using IPSEC may make sense.