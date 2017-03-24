---
layout: post 
title:  "Exchange Best Practices: Client Access Namespaces" 
date:   2017-03-24T15:50:15.650Z 
categories: exchange exchange2016 exchange2013 
link: https://practical365.com/exchange-server/exchange-best-practices-client-access-namespaces/ 
tags:
  - links
ogtype: article 
---

> Exchange Best Practices: Client Access Namespaces
JANUARY 13, 2016   BY PAUL CUNNINGHAM
When deploying Exchange Server 2013 or 2016 there are some best practices to be aware of for your namespace configuration.

Servers within an Active Directory site should have the same namespaces configured
Namespaces should not contain server fully qualified domain names (FQDNs)
Exchange namespaces should be domain names that your organization owns (this is important for DNS resolution, and for SSL certificate requirements)