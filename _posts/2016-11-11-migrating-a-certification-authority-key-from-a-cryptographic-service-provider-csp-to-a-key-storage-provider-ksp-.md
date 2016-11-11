---
layout: post 
published: true 
title: "Migrating a Certification Authority Key from a Cryptographic Service Provider (CSP) to a Key Storage Provider (KSP)" 
date: 2016-11-11T08:21:21.435Z 
link: https://technet.microsoft.com/en-us/library/dn771627.aspx 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Migrating a Certification Authority Key from a Cryptographic Service Provider (CSP) to a Key Storage Provider (KSP)

 
Updated: June 28, 2016
Applies To: Windows Server 2012 R2, Windows Server 2012
If you have installed an enterprise or standalone certification authority (CA) that uses a Cryptographic Service Provider (CSP) for its private key, you might want migrate that key to a software Key Storage Provider (KSP). For example, this migration would then let the CA support the latest enhanced key storage mechanism and stronger key and signature algorithms for Cryptography Next Generation (CNG).
