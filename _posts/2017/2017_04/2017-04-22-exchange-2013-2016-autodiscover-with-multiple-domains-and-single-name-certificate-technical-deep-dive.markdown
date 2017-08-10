---
layout: post 
title:  "Exchange 2013, 2016 - Autodiscover with multiple domains and single name certificate | Technical Deep Dive" 
date:   2017-04-22T14:06:40.809Z 
categories: exchange autodiscover xml outlook scp
link: https://markgossa.blogspot.de/2015/11/exchange-2013-2016-autodiscover-with-multiple-domains-and-single-name-certificate.html 
tags:
  - links
ogtype: article 
---

> Exchange 2013, 2016 - Autodiscover with multiple domains and single name certificate
When setting up multiple email domains, you require a namespace for the Exchange CAS services such as OAB, EWS, Outlook Anywhere and you also need an autodiscover.domain.com A record for each domain that you require autodiscover for. In this post, I’ll demonstrate how you can configure Autodiscover for multiple domains while using only a single name on your 