---
layout: post 
title:  "Exchange Server TLS guidance Part 3: Turning Off TLS 1.0/1.1 – You Had Me At EHLO…" 
date:   2018-07-13T14:37:43.129Z 
categories: exchange exchange2016 security tls
link: https://blogs.technet.microsoft.com/exchange/2018/05/23/exchange-server-tls-guidance-part-3-turning-off-tls-1-01-1/ 
tags:
  - links
ogtype: article 
---

## Exchange Server TLS guidance Part 3: Turning Off TLS 1.0/1.1
★★★★★★★★★★★★★★★
The Exchange TeamMay 23, 20180
Share
126
0
Overview
In part 3 of our Exchange Server TLS Guidance series, we introduce how to turn off TLS 1.0 and 1.1 in your Exchange Server deployment. Turning off TLS 1.0 and 1.1 can be a highly disruptive event if not planned and executed properly. The Exchange team believes that it is time for the ecosystem to fully embrace TLS 1.2, but urges you to proceed with caution when disabling TLS 1.0 and 1.1. This includes understanding how and being prepared to reverse the configuration steps if necessary.

Assumption
Before disabling TLS 1.0 and 1.1, it is important that you have completed the steps outlined in Part 1: Getting Ready for TLS 1.2 and Part 2: Enabling TLS 1.2 and Identifying Clients Not Using It. Do not proceed until you have completed these steps on all Exchange servers, have read all of Part 3 (this post) and understand the implications of disabling TLS 1.0 and 1.1.