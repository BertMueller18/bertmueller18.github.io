---
layout: post 
published: true 
title: "Overlay Tunneling with Open vSwitch - GRETAP, VXLAN, Geneve, GREoIPsec - CostiSer.Ro" 
date: 2016-09-11T21:42:53.249Z 
link: http://costiser.ro/2016/07/07/overlay-tunneling-with-openvswitch-gre-vxlan-geneve-greoipsec/#.V9UZnJOLR-h 
tags:
  - links
ogtype: article 
bodyclass: post 
---

>  SDN Overlay Tunneling with Open vSwitch - GRETAP, VXLAN, Geneve, GREoIPsec
 Thu 07 July 2016     Costi
 SDN
1 Comment
Overlay Tunneling with Open vSwitch - GRETAP, VXLAN, Geneve, GREoIPsec
Initial State
Overlay Tunnels using Open vSwitch
GRETAP
VXLAN
Geneve
GREoIPsec
Building overlay networks using tunnels was always done to achieve connectivity between isolated networks that needed to share the same policies, VLANs or security domains. In particular, they represent a strong use-case in the data center, where tunnels are created between the hypervisors in different locations allowing virtual machines to be provisioned independently from the physical network.