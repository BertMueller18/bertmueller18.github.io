---
layout: post
published: true
title: "How To Create a Redundant Storage Pool Using GlusterFS on Ubuntu Servers | DigitalOcean"
date: 2016-09-12T06:50:17.177Z
categories: gluster ubuntu digitalocean storage
link: https://www.digitalocean.com/community/tutorials/how-to-create-a-redundant-storage-pool-using-glusterfs-on-ubuntu-servers
tags:
  - links
ogtype: article
bodyclass: post
---

## How To Create a Redundant Storage Pool Using GlusterFS on Ubuntu Servers
Posted Feb 5, 2014 127.1k views Scaling Networking Ubuntu
Introduction

Redundancy and high availability are necessary for a very wide variety of server activities. Having a single point of failure in terms of data storage is a very dangerous configuration for any critical data.

While many databases and other software allows you to spread data out in the context of a single application, other systems can operate on the filesystem level to ensure that data is copied to another location whenever it is written to disk. A clustered storage solution like GlusterFS provides this exact functionality.

In this guide, we will be setting up a redundant GlusterFS cluster between two 64-bit Ubuntu 12.04 VPS instances. This will act similar to an NAS server with mirrored RAID. We will then access the cluster from a third 64-bit Ubuntu 12.04 VPS.
