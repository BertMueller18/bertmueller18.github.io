---
layout: post 
title:  "HowTo load balance while preserving a clients source IP but not using the NetScaler as your Gateway | Stefan Holste" 
date:   2017-12-05T16:50:47.602Z 
categories: netscaler exchange exchange2106 loadbalancer
link: http://citrix.stefanriek.de/citrix/howto-load-balance-while-preserving-a-clients-source-ip-but-not-using-the-netscaler-as-your-gateway/ 
tags:
  - links
ogtype: article 
---

# HowTo load balance while preserving a clients source IP but not using the NetScaler as your Gateway

by STEFAN HOLSTE on FEBRUAR 9, 2012 · 27 COMMENTS · in CITRIX, NETSCALER
Recently I had to transfer a NetScaler VPX configuration to a MPX appliance. This was not much of a hassle as most of the configuration can just be re used but be sure to check as i.e. the ntp configuration did not quite reach the new appliance.

Nevertheless as always I was not only applying the old configuration but also doing some optimizing. The number one desire was to use rules with Exchange 2010 SMTP. The challenge was not indeed to create a rule within Exchange but rather that the rule was based on client addresses!

There was already a load balancing virtual server created which worked perfectly but you have to keep in mind that with a standard load balancing virtual server the Exchange servers will always only notice the NetScalers IP address.