---
layout: post
title:  "Flockport Labs - Extending layer 2 across container hosts        "
date:   2016-11-22T22:35:32.963Z
categories: sdn networking linux
link: https://www.flockport.com/flockport-labs-extending-layer-2-across-container-hosts/
tags:
  - links
ogtype: article
---

## Extending layer 2 across container hosts

This post is to consolidate all our LXC networking guides and also explore some advanced container networking that have limited use but are interesting nonetheless hence the Flockport labs monicker. Experimental containers will now be posted under this label in our container section.
We previously looked at basic LXC container networking; bridging, NAT, static IPs, public IPs etc and then at connecting LXC containers across hosts with GRE tunnels or secure Tinc or IPSEC VPNs.

We also covered basic failover and load balancing with Keepalived and Nginx and with LVS. These networking guides apply to both LXC and VM networking in Linux in general with KVM or Xen for instance.

This would be a good time to brush up. This guide explores a few advanced LXC networking possibilities that depend on a fair understanding of LXC and VM networking.

We will cover extending layer 2 across remote LXC hosts with L2tpv3 or Ethernet over GRE in Part I and using LXC's support for multiple network interfaces to explore using a container as a router and touch on using VMs of software routers like Vyatta, Vyos or Pfsense to route your container or VM networks in Part II. We also cover using VXLAN separately.
