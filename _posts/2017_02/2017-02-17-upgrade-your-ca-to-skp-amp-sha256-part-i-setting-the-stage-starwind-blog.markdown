---
layout: post 
title:  "Upgrade your CA to SKP &amp; SHA256. Part I: Setting the Stage | StarWind Blog" 
date:   2017-02-17T21:36:48.105Z 
categories: pki sha256 windows certificate
link: https://www.starwindsoftware.com/blog/upgrade-your-ca-to-skp-sha256-part-i-setting-the-stage 
tags:
  - links
ogtype: article 
---

> Upgrade your CA to SKP & SHA256. Part I: Setting the Stage
Posted by Didier Van Hoye on January 31, 2017	
Tags: Certificate Authority, Microsoft Strong Cryptographic Provider, SCP, server, SHA256, Windows Server 2003, windows server 2016, WS2016
00050
				4.75/5
Introduction

Many Certificate Authority servers that were installed on Windows Server 2003 never got upgraded until Microsoft ceased the support of Windows 2003. Some of those are still out there running today. A massive amount of them got set up in an era when Wi-Fi in the SME market became very popular and CA servers were deployed to easily secure access to it. To be fair, a lot of administrators didn’t wait for Windows Server 2003 support to expire and made sure their CA was more or less up to date by upgrading them in place. That alone is something to commend. However, the operating system version only introduces the capability of using modern more secure providers and algorithms. It doesn’t upgrade the ones used by the PKI automatically for you. So many of these upgrade PKI servers are still using an old cryptographic provider, the “Microsoft Strong Cryptographic Provider” (SCP) and an old hash algorithm (SHA1) that’s been deprecated (see SHA1 Deprecation: What You Need to Know) or even banned.