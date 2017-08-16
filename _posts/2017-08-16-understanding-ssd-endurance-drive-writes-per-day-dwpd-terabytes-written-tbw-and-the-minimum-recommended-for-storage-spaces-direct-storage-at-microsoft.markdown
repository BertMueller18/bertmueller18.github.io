---
layout: post 
title:  "Understanding SSD endurance: drive writes per day (DWPD), terabytes written (TBW), and the minimum recommended for Storage Spaces Direct | Storage at Microsoft" 
date:   2017-08-16T07:52:04.317Z 
categories: storage s2d server2016 windows 
link: https://blogs.technet.microsoft.com/filecab/2017/08/11/understanding-dwpd-tbw/ 
tags:
  - links
ogtype: article 
---

> Understanding SSD endurance: drive writes per day (DWPD), terabytes written (TBW), and the minimum recommended for Storage Spaces Direct
★★★★★★★★★★★★★★★
August 11, 2017 by Cosmos Darwin // 2 Comments

30
0
Hi! I’m Cosmos. Follow me on Twitter @cosmosdarwin.

Background
Storage Spaces Direct in Windows Server 2016 features a built-in, persistent, read and write cache to maximize storage performance. You can read all about it at Understanding the cache in Storage Spaces Direct. In all-flash deployments, NVMe drives typically cache for SATA/SAS SSDs; in hybrid deployments, NVMe or SATA/SAS SSDs cache for HDDs.