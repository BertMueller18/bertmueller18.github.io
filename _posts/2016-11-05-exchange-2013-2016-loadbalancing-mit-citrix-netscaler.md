---
layout: post 
published: true 
title: "Exchange 2013/2016 – Loadbalancing mit Citrix Netscaler" 
date: 2016-11-05T22:33:16.070Z 
link: http://news.digicomp.ch/de/2016/05/18/exchange-20132016-loadbalancing-mit-citrix-netscaler/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Exchange 2013/2016 – Loadbalancing mit Citrix Netscaler
 18. May 2016   Markus Hengstler   IT im Netz   Keine Kommentare
Jetzt Newsletter abonnieren und nichts verpassen! Anmelden
In einem früheren Blog-Artikel habe ich auf die Wichtigkeit von Loadbalancing für Exchange-Umgebungen hingewiesen. Nun sind bei Kunden mit Citrix-XenDesktop-Infrastrukturen normalerweise schon Netscaler Appliances im Einsatz und es ist durchaus sinnvoll, diese auch für Exchange zu verwenden. Citrix hat auch einen Deployment Guide herausgegeben, der die Konfiguration beschreibt und diese vereinfachen sollte. Lassen Sie sich nicht durch den hohen Detaillierungsgrad des Dokuments in die Irre führen – es haben sich einige Fehler und Stolpersteine eingeschlichen, auf die ich in diesem Artikel eingehen möchte.

Ich gehe davon aus, dass die Option Single Namespace / Layer 7 (No Session Affinity) aus dem Guide umgesetzt werden soll, da dies die bevorzugte Variante in Microsofts Preferred Architecture ist. Die Option zeichnet sich dadurch aus, dass der SSL-Verkehr terminiert wird, damit die virtuellen Verzeichnisse in den Requests erkannt und jeweils mit einem dedizierten Healthcheck überprüft werden können: