---
layout: post 
published: true 
title: "Configuring a Personal VPN&nbsp;— Blog :: Ivan Smirnov" 
date: 2016-09-28T18:34:51.966Z 
categories: vpn 
link: https://blog.ivansmirnov.name/configuring-a-personal-vpn/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Configuring a Personal VPN
By Ivan Smirnov Feb 25th 2015 Tags: guide, vpn
I often find myself in the position of wanting to access my computer remotely, be it to grab a file, check the status of a download, or to show off a cool project. However, my network is set up behind multiple routers and firewalls not under my control, so most traditional means of access are not available to me. I could try setting up a plethora of services to work in conjunction, such as a reverse SSH tunnel, TeamViewer, and a bunch of other utilities, but I decided to keep it simple and configure a VPN. The problem is, in order for a VPN to work, I need to have port forwarding set up all the way through our convoluted local network. This poses a problem for me for two main reasons: our local sysadmin doesn't know any of the passwords to the routers, and this would open up a security vulnerability in our network.