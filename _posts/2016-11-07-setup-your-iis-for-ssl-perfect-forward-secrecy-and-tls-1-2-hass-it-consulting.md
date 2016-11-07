---
layout: post 
published: true 
title: "Setup your IIS for SSL Perfect Forward Secrecy and TLS 1.2 | Hass - IT Consulting" 
date: 2016-11-07T08:47:52.089Z 
link: https://www.hass.de/content/setup-your-iis-ssl-perfect-forward-secrecy-and-tls-12 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> 
Setup your IIS for SSL Perfect Forward Secrecy and TLS 1.2

MicrosoftIISSSLPerfect Forward SecrecyPowerShellDownload
This PowerShell script setups your Microsoft Internet Information Server 7.5/8.0/8.5/10 (IIS) on Windows 2008R2/2012/2012R2/2016 to support TLS 1.1 and TLS 1.2 protocol with Forward secrecy. Additionally it increases security of your SSL connections by disabling insecure SSL2 and SSL3 and all insecure and weak ciphers that a browser may fall-back, too. This script implements the current best practice rules.