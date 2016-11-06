---
layout: post 
published: true 
title: "Load Balancing Exchange 2013 With Citrix NetScaler 11 – GET CURIOUS" 
date: 2016-11-05T22:33:33.305Z 
link: http://tedjoffs.com/load-balancing-exchange-2013-with-citrix-netscaler-11/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Load Balancing Exchange 2013 With Citrix NetScaler 11
January 23, 2016 by TKJ365 In NetScaler 2 Comments
Today, I am publishing a small guide written and intended to be used as a starting point for Load Balancing Microsoft Exchange 2013 via Citrix NetScaler 11 Build 64.34 and newer with the following expectations:

Provide Load Balancing (LB) to all Exchange services.
Provide ActiveSync Kerberos Constrained Delegation to function with iPhone, iPad (iOS Configuration Utility or AirWatch), Android (TouchDown Mail Client or AirWatch), or Windows Phone (AirWatch).
Provide service monitors that are in line with Microsoft best practices.
Provide all Exchange services via Content Switching Services (CSS) to only use one IP address.
Utilize responder and rewrite policies and actions to automatically redirect unsecured and root URL connections.
All communication from the client through to the Exchange 2013 servers will be secured.