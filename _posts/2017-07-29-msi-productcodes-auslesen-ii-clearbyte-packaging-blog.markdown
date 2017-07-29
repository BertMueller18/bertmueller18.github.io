---
layout: post 
title:  "MSI Productcodes auslesen II | clearByte Packaging Blog" 
date:   2017-07-29T21:23:57.134Z 
categories: deployment msi powershell
link: http://blog.clearbyte.ch/msi-productcodes-auslesen-ii/ 
tags:
  - links
ogtype: article 
---

> MSI PRODUCTCODES AUSLESEN II
April 2017 | Michael Busslinger

Mittels folgender paar Zeilen Powershell Code, können alle ProductCodes von MSI Installationsdateien in einem Verzeichnis und allen Unterverzeichnissen ausgelesen und im Unterschied zum letzten Artikel in einer GridView angezeigt werden.
ValidateSet

Das eigentliche Auslesen des ProductCodes geschieht mittels der Funktion „get-property“. Diese beinhaltet einen Parameter, bzw. ein sogenanntes ValidateSet. Damit wird eingeschränkt, was abgefragt werden kann und somit zurück gegeben werden kann.


1
[ValidateSet('ProductCode','ProductVersion','ProductName')]
In diesem Fall besteht eine Einschränkung auf die drei Properties ProductCode, ProductVersion und ProductName. Selbstverständlich kann das erweitert oder ganz weggelassen werden.