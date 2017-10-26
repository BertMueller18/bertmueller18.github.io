---
layout: post 
title:  "itToby: Web Application Proxy Server in 2012 R2" 
date:   2017-10-26T07:30:56.487Z 
categories: activedirectory adfs reverseproxy
link: http://blog.ittoby.com/2014/04/web-application-proxy-server-in-2012-r2.html 
tags:
  - links
ogtype: article 
---

> Web Application Proxy Server in 2012 R2
When Microsoft discontinued Threat Management Gateway (which once was Proxy and then ISA server) I must admit I was disappointed; it was a relatively inexpensive authenticated reverse proxy that worked with Exchange Server as well as many other complicated products. In the interim we were told that Unified Access Gateway would be the replacement, but that product isn't as well suited to the task.

Several alternatives are out there, including: Kemp, F5, Nginx, and Squid but either the price or the relative difficulty of setup isn't in line with TMG. Fortunately starting in Windows 2012R2 Microsoft introduced Web Application Proxy which largely fills the gap. 