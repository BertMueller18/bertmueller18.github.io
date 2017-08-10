---
layout: post 
title:  "Exchange 2016: OPNsense, HAProxy und Let's Encrypt - Frankys Web" 
date:   2017-04-27T12:26:19.418Z 
categories: exchange2016 opnsense letsencrypt haproxy exchange
link: https://www.frankysweb.de/exchange-2016-opnsense-haproxy-und-lets-encrypt/ 
tags:
  - links
ogtype: article 
---

> Exchange 2016: OPNsense, HAProxy und Let’s Encrypt
Veröffentlicht am10. April 2017AutorFrank4 Kommentare

OPNSense ist ein Fork der bekannten OpenSource Firewall PFSense, mir persönlich gefällt OPNSense besser, die GUI ist aufgeräumter, es gibt eine REST-Api und die wichtigsten PlugIns sind ebenfalls verfügbar.

Da für OPNSense ein Plugin für HAProxy und auch für Let’s Encrypt existiert, habe ich angefangen diese Kombination in Verbindung mit Exchange 2016 zu testen. OPNSense kann also direkt ein kostenloses Zertifikat von Let’s Encrypt anfordern und kümmert sich dann auch selbstständig um die Erneuerung.

Kostenlose Firewall und kostenlose Zertifikate, hört sich doch gut an. Hier ein erster Test.