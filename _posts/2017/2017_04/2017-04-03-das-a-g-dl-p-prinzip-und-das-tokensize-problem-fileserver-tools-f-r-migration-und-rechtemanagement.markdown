---
layout: post 
title:  "Das A-G-DL-P-Prinzip und das Tokensize-Problem » Fileserver Tools für Migration und Rechtemanagement" 
date:   2017-04-03T08:29:29.511Z 
categories: activedirectory security 
link: http://www.fileserver-tools.com/2013/02/agdlp-prinzip-und-das-tokensize-problem/ 
tags:
  - links
ogtype: article 
---

> Das A-G-DL-P-Prinzip und das Tokensize-Problem
Berechtigungen migrieren - KnowHow und HowTo, Berechtigungen verwalten - KnowHow und HowTo 14. Februar 2013

Die Tokensize:
Ein Problem, mit dem fast alle Unternehmen kämpfen. Es entsteht in den meisten Fällen durch die Einführung von stark gesteuerten Berechtigungen und vor allem dann, wenn die Berechtigungen nach dem A-G-DL-P-Prinzip vergeben werden. Das entspricht zwar der Best-Practice-Empfehlung, aber in einigen Fällen ist A-G-DL-P tatsächlich nicht ratsam, weil die Tokensize bei einzelnen Usern auf eine Größe ansteigen kann, die zu technischen Problemen führt.
In einfachen Fällen braucht nur die maximale Tokensize in der Registry angepasst zu werden, die unterstütz werden soll. Meist gibt es aber Abhängigkeiten von anderen Applikationen, die eine Anmeldung bei Überschreitung einer bestimmten Größe Anpassungen erfordern/unmöglich machen. Hier wären z.B. der IIS oder SharePoint zu nennen, aber auch in anderen Applikationen kann das der Fall sein. Aus diesem Grund müssen bei der Einführung eines neuen Berechtigungskonzeptes bestehende Abhängigkeiten identifiziert und geprüft werden!
Wann kommt es zu Problemen mit dem Token?
A-G-DL-P bedeutet, dass die Berechtigungen nach einer bestimmten Methode vergeben werden:
A = Account, der Mitglied einer
G = Globalen Gruppe ist, die alle User einer bestimmten Abteilung enthält, welche wiederum Mitglieder einer
DL = Domänenlokalen Gruppe sind, die speziell für eine bestimmte Berechtigung erstellt wurde und deshalb in der
P = Permission (ACL) eines Verzeichnisses eingetragen ist.
Diese aufwendige Verschachtelung der Gruppen empfiehlt sich in der Microsoft-Welt neben weiteren Gründen vor allem, um den Überblick über die Berechtigungen zu wahren und die Anzahl der Einträge in der ACL eines Verzeichnisse gering zu halten. Hinzu kommen noch andere technische Hilfsgruppen/Berechtigungen, die man setzen muss, um einen User das Browsen durch das Filesystem zu ermöglichen – die sogenannten „Listberechtigungen“. All diese Gruppen führen dazu, dass ein User sehr schnell in sehr vielen Gruppen Mitglied ist. Im Kerberos-Security-Token sind nicht nur alle direkten Gruppenmitgliedschaften sondern auch die indirekten Mitgliedschaften enthalten.
Wenn man nun z. B. in der vierten Ebene eines Verzeichnisbaumes einem User in 20 Verzeichnissen „Lesen“-Berechtigungen gibt, führt das dann unter Umständen zu folgenden Gruppenmitgliedschaften:
  1 x Gruppenmitglied für die Abteilung
20 x Gruppenmitglied für die Berechtigung „Lesen“
  4 x Gruppenmitglied für die Listberechtigung
In Summe ergeben sich also 25 Gruppenmitgliedschaften, was in kleineren Konstellationen mit Abteilungslaufwerken noch kein Problem ist. Sobald man aber sehr viele Projektlaufwerke hat, kann ein User sehr schnell in 200 oder 300 neuen Gruppen Mitglied sein. Sollte er vorher schon in X Gruppen Mitglied gewesen sein, dann…..
Ist A-G-DL-P dann der richtige Weg?
In einigen Fällen ist es tatsächlich sinnvoll, vom A-G-DL-P-Prinzip abzuweichen, auch wenn von direkten Berechtigungen grundsätzlich abzuraten ist. Denn diese tragen notwendig zur Intransparenz bei, weil man mit Windows-Bordmitteln allein nicht mehr nachvollziehen kann, wo denn ein User tatsächlich überall berechtigt ist.
Das ist nur eine Betrachtung in diesem Zusammenhang. Es lohnt sich, während der Erstellung eines neuen Konzeptes etwas Zeit in dieses Thema zu investieren. In unseren Projekten haben wir Situationen erlebt, in denen für 500 User auf einmal 25.000 Gruppen aufgebaut wurden, um differenziert Berechtigungen zu vergeben…
Es gibt Alternativen wie zum Beispiel:
A-G-G-P/A-G-P
A-G-U-P/A-U-P
Diese Kombinationen wirken sich direkt auf die Tokensize aus, weil die Information zur Gruppe (direkt/indirekte Mitglieschaft) sich im Security Token wiederfindet. Die verschiedenen Gruppentypen beanspruchen folgenden Platz:
Domänen Lokale Gruppe: 40 byte
Globale Gruppe: 8 byte
Universelle Gruppe in eigener Domänen: 8 byte
Universelle Gruppe aus fremder Domäne: 40 byte
Aus diesem Grund kann man sich auch fragen, ob man überhaupt Gruppen verschachtelt oder die User direkte in eine Berechtigungsgruppe eines Verzeichnisse einfüge.