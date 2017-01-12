---
layout: post
published: true
title: "Stop using SMB1 | Server Storage at Microsoft"
date: 2016-09-21T17:41:01.450Z
categories: server2012  
link: https://blogs.technet.microsoft.com/filecab/2016/09/16/stop-using-smb1/
tags:
  - links
ogtype: article
bodyclass: post
---

## Stop using SMB1
★★★★★★★★★★★★★★★
September 16, 2016 by NedPyle [MSFT] // 10 Comments
0
191
0
Hi folks, Ned here again and today’s topic is short and sweet:

Stop using SMB1. Stop using SMB1. STOP USING SMB1!

Earlier this week we released MS16-114, a security update that prevents denial of service and remote code execution. If you need this security patch, you already have a much bigger problem: you are still running SMB1.

The original SMB1 protocol is nearly 30 years old, and like much of the software made in the 80’s, it was designed for a world that no longer exists. A world without malicious actors, without vast sets of important data, without near-universal computer usage. Frankly, its naivete is staggering when viewed though modern eyes. I blame the West Coast hippy lifestyle.

Let me explain why this protocol needs to hit the landfill.
