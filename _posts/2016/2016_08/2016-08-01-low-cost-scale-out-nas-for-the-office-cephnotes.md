---
layout: post 
published: true 
title: "Low Cost Scale-Out Nas for the Office - CephNotes" 
date: 2016-08-01T19:28:55.841Z
categories: linux ceph storage
link: http://cephnotes.ksperis.com/blog/2014/08/07/low-cost-scale-out-nas-for-the-office 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Low Cost Scale-Out Nas for the Office
AUG 7TH, 2014
The aim is showing that it is possible to create a low-cost storage, efficient and scalable, using opensource solutions. In the example below, I am using Ceph for scalability and reliability, combined with EnhanceIO to ensure very good performance.

Architecture

The idea was to create a storage with two parts: the storage itself (backing store) and a large cache to keep good performance on all data actually used. In fact, the volume needs may be important, but in the context of use for office, the data really used every day is only a portion of this storage. In my case, I intend to use Ceph deployed on low-cost hardware to ensure a scalable and reliable conformatble volume, based on small servers with large SATA drives. Data access will be via Samba shares on a slightly more powerful machine with an SAS Array to create a big cache. (Since Firefly, it would be more interesting to use ceph cache tiering)

