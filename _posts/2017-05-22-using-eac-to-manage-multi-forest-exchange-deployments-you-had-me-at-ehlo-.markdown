---
layout: post 
title:  "Using EAC to manage multi-forest Exchange deployments – You Had Me At EHLO…" 
date:   2017-05-22T11:41:08.917Z 
categories: Exchange rbac crossforest
link: https://blogs.technet.microsoft.com/exchange/2012/08/30/using-eac-to-manage-multi-forest-exchange-deployments/ 
tags:
  - links
ogtype: article 
---

## EAC to manage multi-forest Exchange deployments

The Exchange TeamAugust 30, 20123 

Following our last article, introducing the new Exchange Administration Center (EAC), we follow up on how the new EAC makes it really easy to manage multi-forest Exchange deployments.

As described in Deploy Exchange 2010 in a Cross-Forest Topology, Exchange Server 2010 can be deployed in a cross-forest or resource forest topology. For the purpose of this article, we will employ the same approach to deploy a resource forest topology with The New Exchange.

First, let’s setup a resource forest environment as shown below, with a one-way forest trust setup so that Forest B trusts Forest A.