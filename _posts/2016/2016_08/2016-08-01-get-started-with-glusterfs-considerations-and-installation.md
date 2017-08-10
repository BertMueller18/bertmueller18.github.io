---
layout: post 
published: true 
title: "Get started with GlusterFS - considerations and installation" 
date: 2016-08-01T20:03:39.563Z
categories: linux gluster 
link: https://support.rackspace.com/how-to/getting-started-with-glusterfs-considerations-and-installation/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Get started with GlusterFS - considerations and installation
Last updated on: 2016-01-15 Authored by: Marcin Stangel
Before you start to use GlusterFS, you have to make a fundamental decision: what type of volumes do you need for your environment. The following methods are used most often to achieve different results:

Volume type	Description
Replicated	This type of volume provides file replication across multiple bricks. It is the best choice for environments where high availability and high reliability are critical, and when you want to self-mount the volume on every node, such as with a web server document root (the GlusterFS nodes are their own clients). Files are copied to each brick in the volume, similar to a RAID-1. However, you can have 3 or more bricks or an odd number of bricks; usable space is the size of one brick, and all files written to one brick are replicated to all others. This type works well if you are going to self-mount the GlusterFS volume, for example as the web server document root (/var/www) or similar where all files must reside on that node. The value passed to replica is the same number of nodes in the volume. In type of volume, files are distributed across replicated bricks in the volume. You can use this type of volume in environments where the requirement is to scale storage and have high availability. Volumes of this type also offer improved read performance in most environments, and are the most common type of volumes used when clients are external to the GlusterFS nodes themselves.
Distributed-Replicated	Somewhat like a RAID-10, an even number of bricks must be used; usable space is the size of the combined bricks passed to the replica value. For example, if there are 4 bricks of 20 GB and you pass replica 2 to the creation, your files are distributed to 2 nodes (40 GB) and replicated to 2 nodes. With 6 bricks of 20 GB and replica 3, your files are distributed to 3 nodes (60 GB) and replicated to 3 nodes, but if you used replica 2, they are would distributed to 2 nodes (40 GB) and replicated to 4 nodes in pairs. This distribution and replication woul be used when your clients are external to the cluster, not local self-mounts.
All the fundamental work in this document is the same except for the one step where the volume is created with the replica keyword. Using striped-based volumes is not covered.