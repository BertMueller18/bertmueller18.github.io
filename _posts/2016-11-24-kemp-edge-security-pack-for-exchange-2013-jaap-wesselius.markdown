---
layout: post 
title:  "Kemp Edge Security Pack for Exchange 2013 | Jaap Wesselius" 
date:   2016-11-23T23:15:13.577Z 
categories: exchange2013 exchange2016 loadbalancer kemp
link: https://jaapwesselius.com/2013/05/08/kemp-edge-security-pack-for-exchange-2013/ 
tags:
  - links
ogtype: article 
---

> KEMP EDGE SECURITY PACK FOR EXCHANGE 2013
MAY 8, 2013 JAAPWESSELIUS	7 COMMENTS
Now that Microsoft TMG2010 no longer is available it’s time to look for other alternatives. Reverse proxy solutions is not a problem, there are various solutions for this. Microsoft itself has the ARR (Application Request Routing) on top of IIS available. This can perform reverse proxy, but for load balancing you still have to rely on NLB. Another drawback is that ARR does not do pre-authentication.

With the new software version for the Kemp LoadMaster series (V7) it is now possible to do reverse proxy and pre-authentication out of the box. The new module is called ESP or Edge Security Pack. The idea is the same as before, clients hit the Kemp LoadMasters and the requests are distributed across multiple Exchange Client Access Servers. But before the requests are sent to the Client Access Servers they are authenticated. Kemp uses an authentication provider for this, in a normal scenario this would an Active Directory Domain Controller.

