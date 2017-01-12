---
layout: post
published: true
title: "Is low latency enough? Optimizing TCP for optimal ICA traffic | Marius Sandbu"
date: 2016-09-12T22:14:41.942Z
categories:  netscaler ica 
link: http://msandbu.org/is-low-latency-enough-optimizing-tcp-for-optimal-ica-traffic/
tags:
  - links
ogtype: article
bodyclass: post
---

## Is low latency enough? Optimizing TCP for optimal ICA traffic

So I decided to write this blogpost to actually show the effects of TCP optimization on Citrix.
I’ve been stating that you should always change the TCP profile for NetScaler Gateway because the default is BAD.

So therefore I decided to do a bit research to see what kind of effect will a simple TCP profile have on a NetScaler Gateway vServer. A simple setup where I had two NetScaler Gateway virtual server where one has the default TCP profile and another has the nstcp_xa_xd profile. Now I also used NetScaler Insight to follow the latency between the clients and the server. Both using the same version of NetScaler and the same version of Citrix Receiver to connect to both sites.
