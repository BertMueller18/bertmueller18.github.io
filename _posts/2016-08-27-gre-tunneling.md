---
layout: post 
published: true 
title: "GRE tunneling" 
date: 2016-08-27T14:19:58.205Z
categories: linux gre networking
link: http://www.tldp.org/HOWTO/Adv-Routing-HOWTO/lartc.tunnel.gre.html 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## GRE tunneling

GRE is a tunneling protocol that was originally developed by Cisco, and it can do a few more things than IP-in-IP tunneling. For example, you can also transport multicast traffic and IPv6 through a GRE tunnel.

In Linux, you'll need the ip_gre.o module.

5.3.1. IPv4 Tunneling

Let's do IPv4 tunneling first: