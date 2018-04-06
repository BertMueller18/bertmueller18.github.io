---
layout: post 
title:  "Aaron Toponce : ZFS Administration, Part IV- The Adjustable Replacement Cache" 
date:   2018-03-31T13:37:58.812Z 
categories: zfs linux ssdcache
link: https://pthree.org/2012/12/07/zfs-administration-part-iv-the-adjustable-replacement-cache/ 
tags:
  - links
ogtype: article 
---

> ZFS Administration, Part IV- The Adjustable Replacement Cache
Table of Contents
Zpool Administration	ZFS Administration	Appendices
0. Install ZFS on Debian GNU/Linux	9. Copy-on-write	A. Visualizing The ZFS Intent Log (ZIL)
1. VDEVs	10. Creating Filesystems	B. Using USB Drives
2. RAIDZ	11. Compression and Deduplication	C. Why You Should Use ECC RAM
3. The ZFS Intent Log (ZIL)	12. Snapshots and Clones	D. The True Cost Of Deduplication
4. The Adjustable Replacement Cache (ARC)	13. Sending and Receiving Filesystems
5. Exporting and Importing Storage Pools	14. ZVOLs
6. Scrub and Resilver	15. iSCSI, NFS and Samba
7. Getting and Setting Properties	16. Getting and Setting Properties
8. Best Practices and Caveats	17. Best Practices and Caveats
Our continuation in the ZFS Administration series continues with another zpool VDEV call the Adjustable Replacement Cache, or ARC for short. Our previous post discussed the ZFS Intent Log, or ZIL and the Separate Intent Logging Device, or SLOG.

Traditional Caches
Caching mechanisms on Linux and other operating systems use what is called a Least Recently Used caching algorithm. The way the LRU algorithm works, is when an application reads data blocks, they are put into the cache. The cache will fill as more and more data is read, and put into the cache. However, the cache is a FIFO (first in, first out) algorithm. Thus, when the cache is full, the older pages will be pushed out of the cache. Even if those older pages are accessed more frequently. Think of the whole process as a conveyor belt. Blocks are put into most recently used portion of the cache. As more blocks are read, the push the older blocks toward the least recently used portion of the cache, until they fall off the conveyor belt, or in other words are evicted.


Image showing the traditional LRU caching scheme. Image courtesy of Storage Gaga.

When large sequential reads are read from disk, and placed into the cache, it has a tendency to evict more frequently requested pages from the cache. Even if this data was only needed once. Thus, from the cache perspective, it ends up with a lot of worthless, useless data that is no longer needed. Of course, it's eventually replaced as newer data blocks are requested.

There do also exist least frequently used (LFU) caches. However, they suffer from the problem that newer data could be evicted from the cache if it's not read frequently enough. Thus, there are a great amount of disk requests, which kind of defeats the purpose of a cache to begin with. So, it would seem that the obvious approach would be to somehow combine the two- have an LRU and an LFU simultaneously.

The ZFS ARC
The ZFS adjustable replacement cache (ARC) is one such caching mechanism that caches both recent block requests as well as frequent block requests. It is an implementation of the patented IBM adaptive replacement cache, with some modifications and extensions.

Before beginning, I should mention that I learned a lot about the ZFS ARC from http://www.c0t0d0s0.org/archives/5329-Some-insight-into-the-read-cache-of-ZFS-or-The-ARC.html. The following images of that post I am reusing here. Thank you Joerg for an excellent post.

Terminology