---
layout: post 
title:  "User Guide - VyOS" 
date:   2017-03-01T11:10:18.859Z 
categories: networking linux vyatta
link: https://wiki.vyos.net/wiki/User_Guide 
tags:
  - links
ogtype: article 
---

> User Guide
Contents
1	Introduction
2	Installation
3	Using the Command-Line Interface
4	Quick Start Guide
5	Configuration Overview
6	Network Interfaces
6.1	Ethernet Interfaces
6.2	VLAN Sub-Interfaces (802.1Q)
6.3	Bridging
6.4	Bonding
6.5	Tunnel Interfaces
7	Routing
7.1	Static
7.2	RIP
7.3	OSPF
7.3.1	IPv4
7.3.2	IPv6
7.4	BGP
7.4.1	IPv4
7.4.2	IPv6
7.4.3	Route Filtering
7.5	Policy Routing
8	Firewall
8.1	Groups
8.2	Rule-Sets
8.3	Applying a Rule-Set to an Interface
8.4	Applying a Rule-Set to a Zone
8.5	Zone-based Firewall Policy
9	NAT
9.1	Source NAT
9.2	Destination NAT
9.3	1-to-1 NAT
9.3.1	1-to-1 NAT example
9.4	NPTv6 (RFC6296)
10	VPN
10.1	OpenVPN
10.1.1	Site-To-Site
10.2	L2TP over IPsec
10.3	Site-to-Site IPsec
11	QoS and Traffic Policy
12	DHCP Server
13	DHCP-Relay
14	DNS Forwarder
15	Dynamic DNS
16	System Configuration
16.1	System Users
16.1.1	Creating Login User Accounts
16.1.2	Configuring for SSH Access using Shared Public Keys
17	IPv6
18	Clustering
19	System Image Management
20	Troubleshooting
20.1	Basic Connectivity Verification
20.2	Monitoring Network Interfaces
The VyOS User Guide is focused on providing a general overview of the installation, configuration, and operation of the VyOS network operating system.

Introduction
VyOS is a Linux-based network operating system that provides software-based network routing, firewall, and VPN functionality.

The VyOS project was started in late 2013 as a community fork of the GPL portions of Vyatta Core 6.6R1 with the goal of maintaining a free and open source network operating system in response to the decision to discontinue the community edition of Vyatta. Here everyone loves learning, older managers and new users.

VyOS is primarily based on Debian GNU/Linux and the Quagga routing engine. Its configuration syntax and command-line interface are loosely derived from Juniper JUNOS as modeled by the XORP project (which was the original routing engine Vyatta was based upon). Vyatta changed to the Quagga routing engine for release 4.0.
