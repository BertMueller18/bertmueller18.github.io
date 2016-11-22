---
layout: post 
title:  "MSXFAQ.DE:WinHTTP" 
date:   2016-11-22T23:49:55.713Z 
categories: Exchange Windows 
tags:
  - links
ogtype: article 
---

WinHTTP, WinINET und Windows Proxy

Seiteninhalt
HTTP unter Windows
Wer nutzt das ?
Proxyeinstellungen mit WinHTTP
Proxy-Einstellungen in WinINET
Debugging von WinHTTP
Exchange mit HTTPProxy
.NET Code und HTTPProxy
Der Trend ist unübersehbar: HTTPS und HTTP ist das primäre Protokolle zum Übertragen von Daten zwischen Clients und Servern. Und damit meine ich nicht nur das klassische "Surfen" im Web mit den multimedialen Inhalten wie Audio (Internetradio) oder Videos (YouTube und Co). HTTPS wird auch bei der Kommunikation zwischen Servern (Siehe Kalenderfederation) und für die Überprüfung von Zertifikaten (Siehe CRL) genutzt.

Aber auch HTTP hat die Herausforderung Netzwerkgrenzen mit privaten und öffentlichen IP-Adressen und Firewall-Filter zu überspringen. Während im Homeoffice-Bereich dies durch DSL-Router mit NAT noch sehr einfach ist, gilt es bei Firmen durchaus andere Anforderungen zu meistern. Hier ist in der Regel ein HTTP-Proxy im Einsatz, der auf dem Client einmal konfiguriert werden will, der aber zudem auch eine Authentifizierung anfordern kann und die angefragten URLs prüft, filtert und auch die Antworten eventuell auf ihre Gefährlichkeit bewerten kann. Wenn ein Client oder Server aber nur unter Nutzung eines Proxy-Servers externe Dienste ansprechen kann, dann gilt es heraus zu finden, wie dies konfiguriert werden kann.