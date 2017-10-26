---
layout: post 
title:  "AppLocker konfigurieren und verwalten" 
date:   2017-10-24T06:39:42.038Z 
categories: applocker
link: https://www.einfaches-netzwerk.at/applocker-konfigurieren-und-verwalten/ 
tags:
  - links
ogtype: article 
---

> Teil 25: AppLocker konfigurieren und verwalten
Publiziert am 27. Oktober 2014 von Dietmar Haimann
Letztes Update: 4. November 2014

Ab Windows 7 Enterprise kann man AppLocker konfigurieren, um das Ausführen unerwünschter Software im Unternehmen zu verhindern. Unerwünscht hat in diesem Zusammenhang unterschiedliche Bedeutungen:

Schutz gegen unerwünschte Software: AppLocker verhindert das Ausführen unerwünschter Software.
Einhaltung von Lizenzbestimmungen: Das Ausführen einer Software für die Mitglieder einer Sicherheitsgruppe in Active Directory erlauben, allen anderen verbieten.
Softwarestandardisierung: Eine bestimmte Software ab einer bestimmten Version erlauben, andere Versionen verbieten.
In sicheren Umgebungen wird auf einem Referenzrechner die gesamte benötigte Software installiert und eine Art Snapshot erzeugt. Diese Software wird erlaubt und alles andere verboten. Mittels whitelisting werden dann weitere Produkte hinzugefügt. Diese Vorgehensweise finde ich sehr aufwendig.