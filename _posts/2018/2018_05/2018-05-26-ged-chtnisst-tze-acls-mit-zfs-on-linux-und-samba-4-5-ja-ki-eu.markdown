---
layout: post 
title:  "Gedächtnisstütze: ACLs mit ZFS on Linux und Samba 4.5 – Ja-Ki.eu" 
date:   2018-05-26T09:06:02.695Z 
categories: linux samba zfs security
link: https://www.ja-ki.eu/2016/09/19/gedaechtnisstuetze-acls-mit-zfs-on-linux-und-samba-4-5/ 
tags:
  - links
ogtype: article 
---

> Gedächtnisstütze: ACLs mit ZFS on Linux und Samba 4.5
19. September 2016 Jascha Kirchhoff  2 Comments
Dieser Beitrag dient nur als kleine Gedächtnisstütze mit den wichtigsten Parametern zur (Windows-)Konfiguration der Access Control Lists (ACLs) auf einem Samba-Share mit ZFS on Linux als Dateisystem. Ohne diese Settings können die ACLs nicht via Windows Explorer gesetzt werden. Das ist kein Weltuntergang, aber unglaublich lästig. Da die Recherche dazu zeitaufwändiger war, als mir lieb ist, fasse ich die notwendigen Befehle kurz zusammen.