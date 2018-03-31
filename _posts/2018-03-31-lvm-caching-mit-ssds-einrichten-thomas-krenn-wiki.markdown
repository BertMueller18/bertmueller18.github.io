---
layout: post 
title:  "LVM Caching mit SSDs einrichten – Thomas-Krenn-Wiki" 
date:   2018-03-31T13:38:34.373Z 
categories: linux lvm ssdcache
link: https://www.thomas-krenn.com/de/wiki/LVM_Caching_mit_SSDs_einrichten?xtxsearchselecthit=1 
tags:
  - links
ogtype: article 
---

> LVM Caching mit SSDs einrichten
Hauptseite > Themenschwerpunkte > SSD Caching
Dieser Wikiartikel zeigt, wie Sie mittels LVM Cache HDDs, durch Verwendung von SSDs als Caching Devices, beschleunigen können. LVM Cache stellt ein Frontend für den dm-cache Kernel Treiber dar, um eine bequeme Administration zu ermöglichen.

Inhaltsverzeichnis [Verbergen] 
1 LVM Cache Grundlagen
1.1 Caching Strategien
1.1.1 Writethrough
1.1.2 Writeback
1.2 Nomenklatur
1.3 Einschränkungen
1.3.1 Problemlösung
2 Vorbereitungen
2.1 Betriebssystem Installation
2.2 SSD und HDD Caches konfigurieren
2.2.1 Deaktivieren der Caches
2.2.2 Persistentes Setzen der Parameter
2.3 Software RAIDs erstellen
3 LVM Cache einrichten
3.1 Physical devices und Volume Group erstellen
3.1.1 Physical Volumes erstellen
3.1.2 Volume Group erstellen
3.2 Logical Volumes erstellen
3.2.1 OriginLV
3.2.2 CacheDataLV
3.2.3 CacheMetadataLV
3.3 Konvertierung in einen Cache Pool
3.3.1 CachePoolLV erstellen
3.3.2 CacheLV erstellen
4 Ausgabe von lvs
5 Testen des Caches
5.1 dmsetup status des erstellten Caches
6 Einzelnachweise
7 Weitere Informationen
LVM Cache Grundlagen
Im nachfolgenden Abschnitt werden kompakt die LVM Cache Grundlagen erläutert, welche Caching Strategien und Komponenten es gibt. Detailliertere Informationen zu LVM finden Sie im Wikartikel LVM Grundlagen.

Caching Strategien
LVM Cache unterstützt zwei unterschiedliche Cache Strategien, writethrough und writeback. Der Wikiartikel zur alternativen SSD Caching Methode Flashcache geht auf die unterschiedlichen Methoden noch detaillierter ein.

Writethrough
Dieser Modus ist standardmäßig konfiguriert, es handelt sich hierbei um einen reinen Lesecache, er stellt sicher dass alle Daten immer auf beiden Devices geschrieben sind, also auf dem CachePoolLV und auch auf dem OriginLV. Falls bei diesem Modus ein Device des Cache Pools ausfällt, resultiert kein Datenverlust.

Writeback
Dieser Modus verzögert als Schreib- und Lesecache das Zurückschreiben der Daten vom Cache Pool zum OriginLV. Writeback erhöht die Performance, aber der Ausfall eines Caching Devices kann durch das verzögerte Schreiben auf die HDD zu einem Datenverlust führen. Deshalb sollte ein Writeback Cache, wie in der folgenden Beispielkonfiguration, immer als RAID 1 ausgeführt werden. Der writeback Modus kann bei der Anlage des Cache Pools durch folgenden Parameter gesetzt werden:
--cachemode writeback
