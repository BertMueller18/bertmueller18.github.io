---
layout: post 
title:  "How to run pi-hole in a Docker container | Nico Maas" 
date:   2017-11-01T19:18:28.500Z 
categories: docker webapp
link: https://www.nico-maas.de/?p=1525 
tags:
  - links
ogtype: article 
---

> How to run pi-hole in a Docker container

Pihole is an awesome little DNS Server with Blacklists for Ad Sites and the ideal tool to install a small and powerful ad filter for the whole network (Intro Video here).

As diginc designed an Docker Image around the Pihole server (which was normally run on a RPi :)) - and made it x86, you can also run it on your normal Homeserver :)!

Important things just before we start: The Docker container needs to bind to ports 53 (DNS) and 80 (HTTP) - so, if you need to run your own DNS - that could interfere. If you need port 80 for some other website - you'll have to make an reverse proxy.