---
layout: post 
title:  "PowerShell-Module in einem eigenen Unternehmens-Repository verwalten |        heise Developer    " 
date:   2017-07-14T11:26:34.327Z 
categories: powershell programming
link: https://www.heise.de/developer/artikel/PowerShell-Module-in-einem-eigenen-Unternehmens-Repository-verwalten-3759956.html 
tags:
  - links
ogtype: article 
---

## PowerShell-Module in einem eigenen Unternehmens-Repository verwalten
Der Dotnet-Doktor 30.06.2017 12:06 Uhr Dr. Holger Schwichtenberg
Zum Schutz gegen Schadsoftware können Organisationen eigene PowerShell-Modul-Repositories mit solchen PowerShell-Modulen erstellen, die geprüft und freigegeben sind.

Die Windows PowerShell ermöglicht inzwischen, Zusatzmodule aus Internetquellen wie der PowerShell Gallery oder Chocolatey herunterladen. Gerade in Zeiten, in denen immer mehr Schadsoftware im Internet kursiert und Unternehmen zunehmend Opfer von Ransomware werden, ist das Herunterladen ausführbarer Dateien in vielen Unternehmen verboten (so in unserem Unternehmen) und damit auch der Zugang zu Online-Repositories wie der PowerShell Gallery und Chocolatey.

Es besteht die Möglichkeit, auf Basis von NuGet in einem Netzwerkpfad ein eigenes, privates Firmen-Repository für explizit (von einer dafür beauftragten Person oder Gruppe) geprüfte PowerShell-Module einzurichten.