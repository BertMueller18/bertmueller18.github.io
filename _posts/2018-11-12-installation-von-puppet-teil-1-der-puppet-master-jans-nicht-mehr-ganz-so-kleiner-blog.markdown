---
layout: post 
title:  "Installation von Puppet (Teil 1) - Der Puppet Master - Jans nicht mehr ganz so kleiner Blog" 
date:   2018-11-12T13:40:16.789Z 
categories: puppet automation deployment devops
link: https://www.zueschen.eu/installation-von-puppet-teil-1/ 
tags:
  - links
ogtype: article 
---

> Installation von Puppet (Teil 1) – Der Puppet Master
 Jan 23. Oktober 2018 Linux
Puppet ist eine Möglichkeit, wie ich zentralisiert ein Management von Windows, Linux und auf Wunsch auch Mac-Systeme durchführen kann und hat sich neben Tools wie Chef, Ansible und Saltstack seit vielen Jahren am Markt etabliert. Mit Hilfe von Puppet kann nahezu alles erreicht werden: Die Installation von Software, die Konfiguration von Systemen, die Definition von einem gewünschten Zustand, ….

Grundsätzlich gibt es einen oder mehrere Puppet Master-Server, auf dem die Konfiguration gehalten und betrieben wird. Auf den zu verwaltenden Systemen wird ein Puppet Agent installiert, der mit dem Master-Server spricht und nach einer Konfiguration fragt. Ist solch eine Konfiguration vorhanden (z.B. soll immer ein gewünschtes Paket installiert sein), setzt der Agent die gewünschte Konfiguration um. Befindet sich der Server bereits im gewünschten Zustand, wird nichts gemacht. Ändert sich ein Paket, die Version von einem Paket oder es kommt ein zweites hinzu, kann dies zentral auf dem Master konfiguriert werden und nach kurzer Zeit befinden sich alle Server im gewünschten Zustand.

In dieser Blogpost-Reihe beschreibe ich die Installation des Master-Servers, die Installation von dem Puppet-Agent auf einem Demo-System sowie eine Beschreibung, wie man mit der Erstellung und Nutzung der ersten Ressourcen beginnen kann.