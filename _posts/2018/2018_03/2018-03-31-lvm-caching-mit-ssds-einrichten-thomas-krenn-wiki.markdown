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

## LVM Caching mit SSDs einrichten
Hauptseite > Themenschwerpunkte > SSD Caching
Dieser Wikiartikel zeigt, wie Sie mittels LVM Cache HDDs, durch Verwendung von SSDs als Caching Devices, beschleunigen können. LVM Cache stellt ein Frontend für den dm-cache Kernel Treiber dar, um eine bequeme Administration zu ermöglichen.

Caching Strategien
LVM Cache unterstützt zwei unterschiedliche Cache Strategien, writethrough und writeback. Der Wikiartikel zur alternativen SSD Caching Methode Flashcache geht auf die unterschiedlichen Methoden noch detaillierter ein.

Writethrough
Dieser Modus ist standardmäßig konfiguriert, es handelt sich hierbei um einen reinen Lesecache, er stellt sicher dass alle Daten immer auf beiden Devices geschrieben sind, also auf dem CachePoolLV und auch auf dem OriginLV. Falls bei diesem Modus ein Device des Cache Pools ausfällt, resultiert kein Datenverlust.

Writeback
Dieser Modus verzögert als Schreib- und Lesecache das Zurückschreiben der Daten vom Cache Pool zum OriginLV. Writeback erhöht die Performance, aber der Ausfall eines Caching Devices kann durch das verzögerte Schreiben auf die HDD zu einem Datenverlust führen. Deshalb sollte ein Writeback Cache, wie in der folgenden Beispielkonfiguration, immer als RAID 1 ausgeführt werden. Der writeback Modus kann bei der Anlage des Cache Pools durch folgenden Parameter gesetzt werden:
--cachemode writeback
