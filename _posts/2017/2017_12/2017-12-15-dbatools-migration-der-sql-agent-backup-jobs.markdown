---
layout: post 
title:  "dbatools - Migration der SQL Agent Backup Jobs" 
date:   2017-12-15T08:43:19.799Z 
categories: sqlserver maintenance dbatools
link: http://www.sql-aus-hamburg.de/dbatools-migration-der-sql-agent-backup-jobs/ 
tags:
  - links
ogtype: article 
---

# dbatools – Migration der SQL Agent Backup Jobs

 28. Juni 2017  Björn Peters

Man kann denken was man will, aber manchmal muss man über seinen Schatten springen… in der Regel bin ich ein Verfechter des SQL Server eigenen Backups, egal ob Backup to Disc, Backup to URL oder Backup to NetworkShare, aber hier musste ich (leider) nachgeben und die Sicherung mittels 3rd-Party-Tools einrichten. Gesagt… getan…

Bei dem Kunden hatten wir sowieso schon alles auf 3rd-Party-Backup umgestellt, aber nicht auf Backup-Server initiertes Sicherungen, sondern SQL Server initiert. Der SQL Server Agent startet also das jeweilige Backup als Kommandozeilen-Aufruf. Hierzu musste ich also die Sicherungsjobs von einem existierenden Server kopieren und anpassen, sowie alle dazugehörigen SQL Server Objekte. Gestartet habe ich mittels „Create Objects to NewQuery“, erhielt aber die Fehlermeldung, dass die Mail-Komponente bzw Empfänger noch existiert bzw konfiguriert ist. Also musste ich erst die SQL-Mail-Konfiguration übernehmen, hierzu auch noch die Operator übernehmen und wenn wir schon beim Mailing sind, dann kann ich die von Brent Ozar empfohlenen SQL Agent Alerts auch gleich mit migrieren…