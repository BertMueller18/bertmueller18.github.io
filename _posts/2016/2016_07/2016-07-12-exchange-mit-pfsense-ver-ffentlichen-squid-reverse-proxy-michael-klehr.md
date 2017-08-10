---
layout: post 
published: true 
title: "Exchange mit pfSense veröffentlichen (Squid Reverse Proxy) | Michael Klehr" 
date: 2016-07-12T19:15:45.732Z
categories: exchange pfsense loadbalancer
link: http://www.klehr.de/michael/exchange-mit-pfsense-veroeffentlichen-squid-reverse-proxy/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Exchange mit pfSense veröffentlichen (Squid Reverse Proxy)

Die Veröffentlichung von Outlook Web Access, ActiveSync und Outlook Anywhere (RPC over HTTPs) ist mit der pfSense absolut easy einzurichten. Externes Zertifikat im Cert Manager hinterlegen, das Package Squid Proxy 3.1 installieren, ein paar Mausklicks und los geht’s. Ich habe zwar eine virtuelle Maschine in unserer DMZ die diese Freigabe mit mod_proxy_msrpc über Apache regelt, aber in kleineren Umgebungen kann man mit den Bordmitteln der kostenlosen pfSense sehr schnell das gleiche Ergebnis erzielen. Der Kompromiss ist meiner Meinung nach absolut in Ordnung. Also – Let’s Klick and Go: