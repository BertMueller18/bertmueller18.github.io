---
layout: post 
title:  "Windows 10 X64 + X86 Setup-Antwortdateien erstellen – Deutscher Syslinux Blog" 
date:   2018-09-20T14:17:39.731Z 
categories: win10 deployment adk
link: https://www.german-syslinux-blog.de/windows-10-x64-x86-setup-antwortdateien-erstellen/ 
tags:
  - links
ogtype: article 
---

> Windows 10 X64 + X86 Setup-Antwortdateien erstellen
KEINE KOMMENTARE
Ich habe nun schon einige Anleitungen zu dem Thema PXE-Boot erstellt, darunter war auch eine Anleitung, wie man von dort aus über Netzwerk, Windows installieren kann. An sich ist das schon sehr praktisch, wenn jeder Rechner im Netzwerk von diesem PXE-Server aus starten kann und darüber auch Betriebssysteme installiert werden können.

Heute möchte ich Ihnen daher die Verwendung von Antwortdateien näher bringen. Diese werden beispielsweise benötigt, wenn die Installation komplett unbeaufsichtigt vonstatten gehen soll. Es gibt hier allerlei Variationen und es bestünde auch die Möglichkeit, lediglich Teilbereiche zu automatisieren, die sich eigentlich nie besonders ändern.

Ein mögliches Szenario wären beispielsweise Privatkunden-, Geschäftskunden- und Eigene- Installationen. Sie könnten zwar die Sprache automatisiert setzen lassen und manch andere Dinge auch, nur ist es hier meiner Meinung nach nicht immer vorteilhaft automatisch Benutzer erstellen zu lassen. Da jeder Privatkunde auch so seine ganz eigenen Vorlieben hat, trägt man dies besser manuell ein. Wie das letztendlich jeder handhabt, muss ja jeder selber wissen. Ich zeige Euch daher ein paar allgemeingültige Beispiele.