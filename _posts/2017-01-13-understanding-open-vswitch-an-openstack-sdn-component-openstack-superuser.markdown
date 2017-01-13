---
layout: post 
title:  "Understanding Open vSwitch, an OpenStack SDN component - OpenStack Superuser" 
date:   2017-01-13T19:17:09.535Z 
categories: sdn networking openvswitch
link: http://superuser.openstack.org/articles/openvswitch-openstack-sdn/ 
tags:
  - links
ogtype: article 
---

> Understanding Open vSwitch, an OpenStack SDN component
This tutorial covers the basics of OpenVSwitch.

 

Superuser
December 26, 2016
Open vSwitch is an open-source project that allows hypervisors to virtualize the networking layer. This caters for the large number of virtual machines running on one or more physical nodes. The virtual machines connect to virtual ports on virtual bridges (inside the virtualized network layer.)

This is very similar to a physical server connecting to physical ports on a Layer 2 networking switch. These virtual bridges then allow the virtual machines to communicate with each other on the same physical node. These bridges also connect these virtual machines to the physical network for communication outside the hypervisor node.

In OpenStack, both the Neutron node and the compute node (Nova) are running Open vSwitch to provide virtualized network services.