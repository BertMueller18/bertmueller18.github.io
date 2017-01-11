---
layout: post
title:  "The Overhead of Software Tunneling  | Network Heresy"
date:   2016-11-22T23:04:23.159Z
categories: openvswitch networking sdn linux
link: https://networkheresy.com/2012/06/08/the-overhead-of-software-tunneling/
tags:
  - links
ogtype: article
---

## The Overhead of Software Tunneling
Posted: June 8, 2012 | Author: networkheresy | Filed under: network virtualization, Open vSwitch |17 Comments
[This post was written with Jesse Gross, Ben Basler, Bruce Davie, and Andrew Lambeth]

Tunneling has earned a bad name over the years in networking circles.

Much of the problem is historical. When a new tunneling mode is introduced in a hardware device, it is often implemented in the slow path. And once it is pushed down to the fastpath, implementations are often encumbered by key or table limits, or sometimes throughput is halved due to additional lookups.

However, none of these problems are intrinsic to tunneling. At its most basic, a tunnel is a handful of additional bits that need to be slapped onto outgoing packets. Rarely, outside of encryption, is there significant per-packet computation required by a tunnel. The transmission delay of the tunnel header is insignificant, and the impact on throughput is – or should be – similarly minor
