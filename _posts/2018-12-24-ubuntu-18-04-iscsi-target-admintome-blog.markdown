---
layout: post 
title:  "Ubuntu 18.04 iSCSI Target | AdminTome Blog" 
date:   2018-12-24T08:44:53.649Z 
categories: linux ubunti storage iscsi
link: https://www.admintome.com/blog/ubuntu-18-04-iscsi-target/ 
tags:
  - links
ogtype: article 
---

> Ubuntu 18.04 iSCSI Target
September 7, 2018 by Bill Ward
(Last Updated On: October 1, 2018)
In this post, we will configure an Ubuntu 18.04 iSCSI target and manage it using the WebMin web application. You can use this storage for Kubernetes or ESXi.


Currently, I have two ESXi servers that host all of my virtual machines for my home lab.

I want to be able to migrate the virtual machines form one ESXi host to another and vice versa.

The best way to do this is configure network storage and attach that to your ESXi hosts.

This post is a precursor to my building a SAN Server that I will use for my iSCSI storage.