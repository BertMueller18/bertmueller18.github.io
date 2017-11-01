---
layout: post 
title:  "Renewing Exchange 2013 Certificates: SHA-256 Style – Working Sysadmin" 
date:   2017-10-31T09:57:45.227Z 
categories: activedirectory pki certificate exchange exchange2013 exchange2016
link: http://www.workingsysadmin.com/renewing-exchange-2013-certificates-sha-256-style/ 
tags:
  - links
ogtype: article 
---

> Renewing Exchange 2013 Certificates: SHA-256 Style
January 14, 2015Exchange, PKI, Windows CAexchange, pki, windows ca
I recently ran into an issue that I think is actually pretty funny. It was time to renew the publicly trusted certificate that we install on our Exchange 2013 servers that gets tied to SMTP, OWA and some other IIS services like autodiscover. Since SHA-1 is on the road to deprecation, our cert vendor pushed pretty hard to get something with a hashing algorithm of SHA-2 (or SHA-256, it’s the same thing). Sounds reasonable, right?

Well, here’s the problem. Even though Microsoft is one of many vendors who is pushing the deprecation of SHA-1, Exchange 2013 doesn’t seem to have a mechanism built into it that generates a SHA-2 cert request. Even the New-ExchangeCertificate PowerShell command doesn’t have a way to change which hashing algorithm is used. Windows 2008 R2 and later support SHA-2 but at the time of writing this article, Exchange 2013 doesn’t have a way to generate such a request.

