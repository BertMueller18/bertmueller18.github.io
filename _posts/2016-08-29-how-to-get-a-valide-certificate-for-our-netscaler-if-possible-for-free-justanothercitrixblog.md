---
layout: post 
published: true 
title: "How to get a valide certificate for our NetScaler, if possible for free? – JustAnotherCitrixBlog" 
date: 2016-08-29T03:35:42.718Z 
link: http://blog.norz.at/netscaler-certificates/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> How to get a valide certificate for our NetScaler, if possible for free?
 Jochy    January 3, 2016   5 Comments on How to get a valide certificate for our NetScaler, if possible for free?
This is an updated blog entry. I first posted it on my old and discontinued blog at blog.com for Citrix NetScaler 10, this one is for Citrix NetScaler 11.

We all know how to get a private Certificate for free: You just have to set up a Windows Server, add a role, select certificate authority. That’s it. However these Certificates are not trusted by any browser, even worse: they are not trusted by our Citrix Receiver too, and therefore it’s impossible to connect to a Citrix XenDesktop of Citrix XenApp server without additional interaction. We have to add the root certificate into our client’s machine. This is not a big issue for a administrator, but it is a big challenge for a normal user. That’s why I prefer to use trusted certificates with my NetScaler: No troubles with untrusted workstations and uneducated users.

