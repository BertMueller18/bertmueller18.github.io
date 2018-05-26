---
layout: post 
title:  "ZFS: auto-snapshots and Windows shadow copies with Samba" 
date:   2018-05-26T09:18:56.600Z 
categories: zfs linux samba snapshot vss
link: https://blog.chaospixel.com/linux/2017/09/zfs-auto-snapshots-and-windows-shadow-copies-with-samba.html 
tags:
  - links
ogtype: article 
---

> ZFS: auto-snapshots and Windows shadow copies with Samba BY DANIEL VOGELBACHER ON SEPTEMBER 1, 2017
With ZFS snapshots and Samba’s shadow_copy2 module, you can expose snapshots to Windows clients as shadow copies.

First, install zfs-auto-snapshot on Debian:

apt-get install zfs-auto-snapshot

Default configuration for zfs-auto-snapshot uses specific labels like daily, weekly etc. This is incompatible to samba’s expected snapshot format. As a good workaround, instead of using text labels, I’ve changed the labels to numbers:

