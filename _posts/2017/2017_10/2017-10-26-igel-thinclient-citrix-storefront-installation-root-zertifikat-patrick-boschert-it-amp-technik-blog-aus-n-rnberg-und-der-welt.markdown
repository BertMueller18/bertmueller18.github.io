---
layout: post 
title:  "IGEL ThinClient + Citrix StoreFront Installation – Root Zertifikat | Patrick Boschert - IT &amp; Technik Blog aus Nürnberg und der Welt" 
date:   2017-10-26T07:22:08.144Z 
categories: igel thinclient citrix certificate
link: http://boschert-consulting.com/igel-thinclient-citrix-storefront-installation-root-zertifikat/ 
tags:
  - links
ogtype: article 
---

> IGEL THINCLIENT + CITRIX STOREFRONT INSTALLATION – ROOT ZERTIFIKAT

Von Patrick Boschert   geschrieben am 11. März 2016   in Thin Clients & Virtualisierung  4
Heute geht es um die Inbetriebnahme von IGEL ThinClients zusammen mit Citrix StoreFront (XenDesktop 7), die zu Beginn kleine Probleme bereiten kann.

Einige erhalten bei den ersten Schritten Fehlermeldungen wie z.B.

1
Error in connection, error given: AM_ERROR_AUTH_AUTH_SERVER_ERROR[65268]
2
Error adding store: Adding new store:AM_ERROR_AUTH_NETWORK_ERROR[65275]
3
Error adding store: Adding new store:AM_ERROR_AUTH_NETWORK_ERROR[65150]
Bei ersterem stimmen die Store-Angaben im Profil oder die Citrix Receiver Version meist nicht. Bei letzten beiden hängt es wohl am Zertifikat.