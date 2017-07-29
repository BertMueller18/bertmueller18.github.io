---
layout: post 
title:  "Installierte Apps PowerShell | clearByte Packaging Blog" 
date:   2017-07-29T21:24:52.631Z 
categories: powershell automation
link: http://blog.clearbyte.ch/mit-powershell-alle-installierten-applikationen-anzeigen/ 
tags:
  - links
ogtype: article 
---

## MIT POWERSHELL ALLE INSTALLIERTEN APPLIKATIONEN ANZEIGEN
Juli 2016 | Michael Busslinger

Es gibt viele Wege eine Liste aller installierten Applikationen mit Powershell zu erstellen. Keine davon hat mir gefallen. Darum habe ich habe mal folgendes Script erstellt, welches die Uninstall Registry Keys sowohl des 64bit als auch des 32bit Bereichs ausliest und übersichtlich darstellt.
Zuerst habe ich einen Array erstellt, welcher die beiden auszulesenden Keys enthält.


1
$appsLookUp = @('HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\*','HKLM:\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall\*')
Danach wird mit einer foreach Schleife der Array abgearbeitet und jeweils mit Get-ItemProperty die gewünschten Infos ausgelesen. Selbstverständlich hätte das ganze auch ohne Schleife mit zweimaligem Aufruf von Get-ItemProperty gelöst werden können. Allerdings hätte das keinen Spass gemacht 

Um den Output übersichtlicher zu halten, habe ich mittels Select-Object nur einige Spalten anzeigen lassen. Für mich war wichtig, auf den ersten Blick zu sehen, aus welchem Bereich der jeweilig Eintrag stammt. Daher habe ich eine eigene Spalte „Registry“ erstellt.


1
@{l="Registry";e={$app}}
Zum Schluss wurden dann noch alle Zeilen mit leerem DisplayName aussortiert.


1
Where {$_.DisplayName -notlike $null}
Weil sich das Resultat schön filtern und sortieren lässt, habe ich Out-GridView gewählt um das ganze anzuzeigen.