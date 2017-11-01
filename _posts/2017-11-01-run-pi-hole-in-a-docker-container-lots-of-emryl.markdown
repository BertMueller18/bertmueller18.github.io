---
layout: post 
title:  "Run Pi-Hole in a Docker Container | Lots of emryl" 
date:   2017-11-01T19:19:50.199Z 
categories: docker
link: http://blog.rylander.io/2017/06/15/run-pi-hole-in-a-docker-container/ 
tags:
  - links
ogtype: article 
---

> Run Pi-Hole in a Docker Container
2017-06-15 DNSDOCKER
I’m probably one of the last to setup a pi-hole and still not convinced it’s such a good idea. Will evaluate for a few weeks and then decide on what to do.

The pi-hole is setup as the primary DNS service for all DHCP connected devices. It will forward to my internal DNS (Windows AD) infrastructure which in turn forwards to the router (UBNT EdgeRouter). The Firewall forwards to OpenDNS. For the rylander.io domain, my internal DNS has a split personality and serveral sub domains are delegated to Cloudflare DNS which also duplicates some hostnames due to LetsEncrypt validation.