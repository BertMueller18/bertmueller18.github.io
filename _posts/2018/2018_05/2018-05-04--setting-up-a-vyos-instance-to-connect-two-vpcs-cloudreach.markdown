---
layout: post 
title:  " Setting up a VyOS instance to connect two VPCs - Cloudreach" 
date:   2018-05-04T12:14:08.076Z 
categories: vyos networking vpn cloud
link: https://www.cloudreach.com/blog/setting-vyos-instance-connect-two-vpcs/ 
tags:
  - links
ogtype: article 
---

## Setting up a VyOS instance to connect two VPCs
 Dimitrios Karagiannis  25th June 2014

Creating multiple Virtual Private Clouds (VPC) in your AWS environments is a very common method of isolating different environments of your estate (which you would want to do for security reasons).


Although VPC Peering is quick and simple to setup, it comes with several routing restrictions. The way around it is what used to be the standard to connect two Virtual Private Clouds: using a virtual appliance to establish an IPsec VPN tunnel between the two. In this post we explore VyOS as a solution for the virtual appliance; VyOS is a fork of the old Vyatta Community Edition and is currently actively developed. You can find it on the AWS marketplace.

Consider the setup below for a site-to-site IPsec configuration between two VPCs