---
layout: post 
title:  "Linux - DM-Cache" 
date:   2018-04-03T20:30:22.537Z 
categories: linux ssd cache lvm 
link: http://www.ahammer.ch/141 
tags:
  - links
ogtype: article 
---

## Device Mapper Cache
Recent device mapper allows to use small SSD disks to cache bigger, much slower conventional disks.

CentOs 7.4
It seems they found a performance bottleneck. Presumable it has a connection to the former message
dmesg output: [device-mapper: cache: You have created a cache device with a lot of individual cache blocks]
but as it wasnt explained anywhere - why should anyone change something....
See LVM Cache: limit number of cache chunks to the amount tested

This explains the following message during configuring a 470GByte cache volume
 # lvconvert --type cache-pool --poolmetadata /dev/vg00/lvol-meta --cachemode writethrough /dev/vg00/lvol-cache
  Using 512.00 KiB chunk size instead of default 64.00 KiB, so cache pool has less then 1000000 chunks.
display the current chunk size
# lvs -o+chunksize
  LV    VG   Attr       LSize Pool         Origin        Data%  Meta%  Move Log Cpy%Sync Convert Chunk
  lvol0 vg00 Cwi-aoC--- 1.81t [lvol-cache] [lvol0_corig] 15.07  0.55            0.00             512.00k
Updates [20170916]
New version of lvmcache-statistics.sh with more details and updated policies
Fixed a typo in the cache device detection.

ATTENTION
Upgrading an LVM cache installation from LVM <2.02.112 to 2.0.112 or even 114 will break the setup. 
The VG cannot be (fully) activated any more.