---
layout: post 
published: true 
title: "Renewing Exchange 2013 Certificates: SHA-256 Style – Working Sysadmin" 
date: 2016-11-03T07:44:35.573Z 
link: http://www.workingsysadmin.com/renewing-exchange-2013-certificates-sha-256-style/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

Renewing Exchange 2013 Certificates: SHA-256 Style
January 14, 2015Exchange, PKI, Windows CAexchange, pki, windows ca
I recently ran into an issue that I think is actually pretty funny. It was time to renew the publicly trusted certificate that we install on our Exchange 2013 servers that gets tied to SMTP, OWA and some other IIS services like autodiscover. Since SHA-1 is on the road to deprecation, our cert vendor pushed pretty hard to get something with a hashing algorithm of SHA-2 (or SHA-256, it’s the same thing). Sounds reasonable, right?

Well, here’s the problem. Even though Microsoft is one of many vendors who is pushing the deprecation of SHA-1, Exchange 2013 doesn’t seem to have a mechanism built into it that generates a SHA-2 cert request. Even the New-ExchangeCertificate PowerShell command doesn’t have a way to change which hashing algorithm is used. Windows 2008 R2 and later support SHA-2 but at the time of writing this article, Exchange 2013 doesn’t have a way to generate such a request.

There are other ways to generate cert requests, though. Since Windows Server 2012 R2 supports SHA-2, and even SHA-2 certificates, perhaps – I thought – the Certificates MMC can be used to generate such a cert. I was right, it can be used to generate a SHA-2 cert. “Great!” I can hear you exclaim, “Now give me the steps on how to do it!” Not so fast. I’m not going to put the full steps to generating a SHA-2 certificate using the Windows Certificates MMC here because of a problem.