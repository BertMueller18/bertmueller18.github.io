---
layout: post
title:  "Configure Kemp Load Balancer for Exchange 2016"
date:   2016-12-17T09:51:41.764Z
categories: exchange exchange2016 loadbalancer kemp
link: https://supertekboy.com/2015/11/17/configure-kemp-load-balancer-for-exchange-2016/
tags:
  - links
ogtype: article
---

## Configure Kemp Load Balancer for Exchange 2016
November 17, 2015 By Gareth Gudger 36 Comments

454 SHARES
Share
Tweet
+1
Share
Reddit
With each release of Exchange we have seen a substantial shift in the way it required load balancers to be configured. For example, between Exchange 2010 and 2013 the requirement for session affinity was dropped. This allowed multiple requests from a single client to take different paths to its mailbox. It no longer mattered which client access servers in a site were involved in the session. This was a contrast to 2010 where a client session had to maintain a single path at all times. Ross Smith covers this in greater detail here.
