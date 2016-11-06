---
layout: post 
published: true 
title: "Langlitz – IT Consulting  » Blog Archive   » How to – Passwort Hashes aus Active Directory auslesen" 
date: 2016-10-12T20:38:45.046Z 
link: http://blog.langlitz-it.de/?p=1592 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> How to – Passwort Hashes aus Active Directory auslesen

Posted by blog@langlitz-it.de on September 9th, 2016

Die Passwort Hashes der AD User auszulesen, stellt sich leichter dar als vermutet. Natürlich sind diese Hashes nicht in Klartext umzuwandeln, aber diese als Hashes wieder in eine neue/andere Umgebung einzulesen, sollte auf diesem Wege möglich sein.

Zunächst wird ein Abbild der NTDS.dit Datenbank benötigt, in der diese Hashes abgelegt sind. Dies lässt sich über NTDSUtil realisieren. Der entsprechende Befehl lautet:

ntdsutil “ac i ntds” “ifm” “create full c:\temp” q q 

Anstelle von C:\Temp können Sie natürlich jedes beliebige Verzeichnis wählen.