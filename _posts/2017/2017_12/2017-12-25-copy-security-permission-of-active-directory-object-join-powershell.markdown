---
layout: post 
title:  "Copy Security permission of active Directory object | Join-PowerShell" 
date:   2017-12-25T22:48:14.391Z 
categories: activedirectory powershell security
link: http://joinpowershell.de/de/2017/11/04/copyadpermissions/ 
tags:
  - links
ogtype: article 
---

> Join-PowerShell Der einfache Weg in die PowerShell
Springe zum Inhalt
Start-Blog
Get-LastPosts
Praktische Ein – und Mehrzeiler
$env:USERPROFILE
Get-NewsOfTheWeek
← Azure Datenbank anlegen und mit PowerShell oder Visual Code bearbeiten.PowerShell Studio 2017 – Grundlagen Debugging →
Sicherheitsberechtigungen von AD-Objekten kopieren
Publiziert am 4. November 2017 von Andreas Bittner
Ab und an kommt es vor, dass die Sicherheitsbestimmungen von Gruppen oder anderen AD-Objekten angepasst werden müssen. Für ein einzelnes Objekt mag das gehen, aber wenn dies für sehr viele umgesetzt werden muss, macht das per Hand keinen Spaß.

Am einfachsten ist es ein AD-Objekt so zu konfigurieren und diese Einstellungen dann zu kopieren. In diesem Beispiel soll die Kennung ‚sorglossu’ Ändern-Rechte auf Gruppen bekommen.

Muster Berechtigungen erstellen