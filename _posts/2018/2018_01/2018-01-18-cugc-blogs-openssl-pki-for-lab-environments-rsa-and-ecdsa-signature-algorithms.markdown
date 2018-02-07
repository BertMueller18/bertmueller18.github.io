---
layout: post 
title:  "CUGC : Blogs : OpenSSL PKI for Lab Environments - RSA and ECDSA Signature Algorithms" 
date:   2018-01-18T22:05:44.855Z 
categories: pki security openssl docker certificate
link: https://www.mycugc.org/blog/openssl-pki-for-lab-env-rsa-and-ecdsa-signature-algorithms?source=1 
tags:
  - links
ogtype: article 
---

## OpenSSL PKI for Lab Environments - RSA and ECDSA Signature Algorithms

Matt Bodholdt
OpenSSL PKI for Lab Environments - RSA and ECDSA Signature Algorithms
Matt Bodholdt - Jan 2018
In lab situations, it is often necessary to utilize SSL certificates to facilitate realistic testing. This isn't always the easiest thing to accomplish and I've seen many engineers over the years fall back to utilizing built-in, self signed certificates on a product to product basis. This makes testing effectively extremely difficult, if not impossible, and often results in time wasted troubleshooting issues that likely wouldn't be issues in an enterprise environment. The solution to this problem is to create your own Public Key Infrastructure (PKI) that allows the functionality found in enterprise or commercial PKI environments. Luckily, this can be done fairly easily, at no cost, if you already have compute space and a little time.