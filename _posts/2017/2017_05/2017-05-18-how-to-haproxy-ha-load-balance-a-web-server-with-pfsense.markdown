---
layout: post 
title:  "How to HAProxy HA/ load balance a web server with pfSense" 
date:   2017-05-18T05:15:47.227Z 
categories: pfsense haproxy reverseproxy
link: https://www.servethehome.com/how-to-haproxy-ha-load-balance-a-web-server-with-a-pfsense-sg-4860/ 
tags:
  - links
ogtype: article 
---

## How to HAProxy HA/ load balance a web server with a pfSense SG-4860
By Patrick Kennedy - November 10, 20151
Share on Facebook Tweet on Twitter  

pfSense HTTP HAProxy - game plan overview
This guide will show you how to use the pfSense HAProxy package to get HA working with your web server. As a response to a forum member request, we are going to show how one can turn two virtual machines into a load balanced HA set. There are many guides out there but they tend to be from older package versions. We are using the pfSense SG-4860 1U which has an Intel Atom C2558 onboard in one of our datacenter labs. The pfSense SG-4680 has QuickAssist so it can handle decent SSL offload as well. In this article, we will be primarily concerned with simple HTTP traffic but HTTPS offload is on our list of to-dos as well. We are using the latest pfSense 2.2.5 release with the HAProxy-1_5 package. It is possible to run a FreeBSD jail with HAProxy or run it on another VM, however we are going to use the pfSense VM to serve the traffic.