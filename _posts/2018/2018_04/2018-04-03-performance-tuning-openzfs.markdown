---
layout: post 
title:  "Performance tuning - OpenZFS" 
date:   2018-04-03T20:29:39.090Z 
categories: zfs performance
link: http://open-zfs.org/wiki/Performance_tuning 
tags:
  - links
ogtype: article 
---

> Basic concepts
Descriptions of ZFS internals that have an effect on application performance follow.

Adaptive Replacement Cache
For decades, operating systems have used RAM as a cache to avoid the necessity of waiting on disk IO, which is extremely slow. This concept is called page replacement. Until ZFS, virtually all filesystems used the Least Recently Used (LRU) page replacement algorithm in which the least recently used pages are the first to be replaced. Unfortunately, the LRU algorithm is vulnerable to cache flushes, where a brief change in workload that occurs occasionally removes all frequently used data from cache. The Adaptive Replacement Cache (ARC) algorithm was implemented in ZFS to replace LRU. It solves this problem by maintaining four lists:

A list for recently cached entries.
A list for recently cached entries that have been accessed more than once.
A list for entries evicted from #1.
A list of entries evicited from #2.
Data is evicted from the first list while an effort is made to keep data in the second list. In this way, ARC is able to outperform LRU by providing a superior hit rate.

In addition, a dedicated cache device (typically a SSD) can be added to the pool, with zpool add poolname cache devicename. The cache device is managed by the L2ARC, which scans entries that are next to be evicted and writes them to the cache device. The data stored in ARC and L2ARC can be controlled via the primarycache and secondarycache zfs properties respectively, which can be set on both zvols and datasets. Possible settings are all, none and metadata. It is possible to improve performance when a zvol or dataset hosts an application that does its own caching by caching only metadata. One example is PostgreSQL. Another would be a virtual machine using ZFS.