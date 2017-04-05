---
layout: post 
title:  "Erklärung was das AGDLP Prinzip bei Microsoft heisst, und warum es Sinnvoll ist" 
date:   2017-04-03T08:26:54.835Z 
categories: activedirectory security 
link: https://www.w3-creative.de/menu-inhalt/windows/agdlp/ 
tags:
  - links
ogtype: article 
---

## Was ist AGDLP

AGDLP heisst erstmal aufgelöst:
Account
Global
Domainlocal
Policy
Das beschreibt die von Microsoft präferierte Methode um Rechte zu vergeben. In einer Active-Directory Domäne.
Das Active-Directory basiert erstmal darauf, daß es nur 1 zentrale Instanz gibt, die Authentisierung ermöglicht. Auch wenn man nun mehrere AD DC (Active-Directory Domain Controller) hat, hat man nur 1 Datenbank.
Das Active-Directory ist erstmal eine Mischung aus LDAP, Kerberos, DNS und diversen Microsoft Erweiterungen. Wie z.b. den GPOs.
LDAP ist eine Datenbank, die auf Lesen optimiert ist. Darin werden u.a. Account Informationen, Konfigurations Informationen gespeichert.
Kerberos ist ein Dienst der Authentisierung zur Verfügung stellt, das ganze allerdings über ein als unsicher eingestuftes Netzwerk.
Weiter wird in einem AD Netzwerk jeder Windows Client als Resource angesehen, und jeder Client fragt normalerweise immer seinen AD DC, ob etwas erlaubt ist oder nicht. Beispielsweise das öffnen einer Datei im NTFS Dateisystem. Dort existieren dann ACL (Access Controll Lists) die die Zugriffe auf eine Datei regeln. Normalerweise wird ein solcher Zugriff per Gruppe geregelt.
Das bedeutet dann dass eine Person in einer entsprechenden Gruppe sein muß, um Zugriff zu bekommen. Das wird dann entweder vom lokalen Fileserver gecacht, oder er fragt eben beim DC an.
Das interessante an der Sache ist nun, daß sich ein Benutzer nur 1 mal am Client anmelden muß. Klappt der Login, bekommt der Benutzer einen Sicherheits Token, mit der Client zukünftig arbeitet. Es ist also keine zusätzliche Anmeldung am Fileserver notwendig. Die Authorisierung übernimmt das Token während der Arbeit.
Bei der Rechtevergabe wird davon ausgegangen, daß eine Freigabe mit Vollzugriff auf die eingebaute Gruppe jeder freigegeben ist. Damit wird dann die Rechteverwaltung komplett über das Snapin Active-Directory Benutzer und Gruppen geregelt. Genauer gesagt wird die Rechteverwaltung allein auf Gruppenebene realisiert. Die NTFS Rechte im Filesystem werden nur 1 Mal aufgebaut.
Weiter kann die Rechtevergabe auf folgenden Überlegungen basieren:
Da die Rechte im Filesystem kumulativ (ergänzend) sind, können die Rechte nach der Freigabe benannt werden und relativ fein aufgsplittet werden:
DL_<FreigabeName>_lesen
DL_<FreigabeName>_schreiben
DL_<FreigabeName>_löschen
DL_<FreigabeName>_Vollzugriff
Der Rechtename sieht so seltsam aus, da er entsprechend den einzellnen Rechten (die sich ja ergänzen) einzellne Gruppen benötigt. Die Gruppen sind dabei Domänenlokal, da es nur Sinn macht DL Gruppen ACL zu geben.
Diese Domänenlokalen Gruppen werden dann entsprechend AGDLP in Globalen Gruppen zusammengefaßt.
Dabei muß man weiter sehen, daß domänenlokale Gruppen nur in der entsprechenden Domäne vorhanden sind. Nur dort werden sie gebraucht.
Globale Gruppen hingegen sind im gesammten Sicherheitskontext einer Domäne vorhanden.

Es kann also z.b. die Gruppe G_Abteilungsleiter geben, die den Gruppen
DL_<FreigabeName>_lesen
DL_<FreigabeName>_schreiben
DL_<FreigabeName>_löschen
angehört.
Die Gruppe G_Verkäufer z.b. gehört dann nur den Gruppen
DL_<FreigabeName>_lesen
DL_<FreigabeName>_schreiben
an, da die Verkäufer halt keine Belege löschen dürfen.
Die entsprechenden Accounts werden dann entsprechend den G_Gruppen zugeordnet.
Das mag zu Anfang etwas kompliziert aussehen (ist es ja auch) aber mit einem solchen Konstrukt kommt man eventuell um explizietes DENY rum. Dann nämlich wenn wenn einem der Abteilungsleiter kein Löschrecht geben will. Dann macht man einfach eine neue globale Gruppe auf , weisst der globalen Gruppe nur die lesen und schreiben DL Gruppe zu. und gut ist.
Die Alternative ist ein explizietes DENY auf eine Person. Oder auf eine Gruppe, wenn man da dann schon mit Gruppen. Schlimmstenfalls muss man auch noch die die NTFS Rechte ändern, da man den Fall nicht bedachte hat.
Mit AGDLP wird alles "on the FLy" entschieden. Das sollte der Server schaffen.
