---
layout: post 
published: true 
title: "brain floss: HTTP Reverse Proxy using Citrix NetScaler VPX Express" 
date: 2016-09-15T14:03:14.263Z 
link: http://blog.millard.org/2014/02/http-reverse-proxy-using-citrix.html 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> HTTP Reverse Proxy using Citrix NetScaler VPX Express
Part 4 in a series
So far: the first three parts of this series dealt with the introduction of a problem (multiple servers behind a NAT firewall that use the same port) and solution (Citrix NetScaler VPX Express); laying the groundwork for configuring the solution; an overview of what we'll be configuring.

Because it is possible to set up content switching with a single host (the degenerate case), this is the method we'll begin with. While it doesn't really do much for us, simply repeating the steps for a second (and subsequent) will result in a working solution. Other guides lay down the steps with two hosts already in mind, and teasing apart the pieces to apply it to your situation might be more difficult.
