---
layout: post 
title:  "Elastic Stack (ELK) Installation und Einrichtung - ELK Stack" 
date:   2018-03-25T15:50:43.450Z 
categories: elkstack automation
link: https://www.technik-finanzen.de/de/elastic-stack-elk-installation-und-einrichtung-logstash-elasticsearch-kibana-und-beats/ 
tags:
  - links
ogtype: article 
---

> Elastic Stack (ELK) Installation und Einrichtung – ELK Stack
  19. DEZEMBER 2016 LINUX
Elastic Stack (Logstash, Elasticsearch, Kibana und Beats)
Der Elastic Stack (auch unter ELK Stack bekannt), ist eine Ansammlung von Services des Unternehmens elastic zum zentralen Sammeln und Auswerten von Log Daten.

Ich beschäftige mich in letzter zeit häufig mit diesem Thema.
Daher möchte ich hier eine kurze Anleitung liefern, wie man einen solchen Server für Testzwecke einrichtet.

Um einen Zentralen Logging Server zu betreiben, benötigt man mehrere Komponente von elastic.
Von einem Elastik Stack spricht man, wenn alle Komponenten auf einem Server laufen.
Dieser Elastic Stack Server stellt alle notwendigen Services zur Sammlung, Filterung und Auswertung von Log Daten bereit.

Die Services bestehen aus:

Kibana = Eine Web Übersicht mit eigens zu erstellenden Dashboards mit Graphen und Tabellen.
Logstash = Empfängt die Logeinträge und Filtert diese, danach werden diese zur ElasticSearch DB weitergeleitet.
ElasticSearch =  Suchmaschinen DB mit der sich der Datenbestand durchsuchen und analysieren lässt.
Beats = Agent Service auf den zu überwachenden Clients. Überträgt z.B. Log Files zu Logstash.
Neben diesen Services gibt es z.B. WinLogBeat – zum erfassen von Windows Logs oder PacketBeat zur Netzwerkanalyse.
Diese Services werden bei elastic alle unter dem namen Beats vertrieben.