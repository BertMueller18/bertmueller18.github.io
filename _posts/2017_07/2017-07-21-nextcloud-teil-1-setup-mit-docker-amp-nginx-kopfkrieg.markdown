---
layout: post 
title:  "Nextcloud Teil 1: Setup mit Docker &amp; Nginx | KopfKrieg" 
date:   2017-07-21T09:13:21.194Z 
categories: docker nextcloud linux
link: https://kopfkrieg.org/2017/06/15/nextcloud-docker-nginx/ 
tags:
  - links
ogtype: article 
---

## Nextcloud Teil 1: Setup mit Docker & Nginx

Ich bin ja gerne Herr über meine Daten, und das betrifft selbstverständlich auch das Thema Cloud. Daten im internen Netzwerk synchronisere ich nun schon seit längerer Zeit via Syncthing, doch Kontakte, Kalender und Notizen bleiben damit außen vor. Weiteres Problem: Ich kann nicht unterwegs auf Daten zugreifen die noch auf dem Server liegen, denn Syncthing synchronisiert entweder ganz oder gar nicht, später herunterladen ist nicht.

Weiteres Problem: Ich habe keine großartige Lust erst dutzende Pakete zu installieren um dann noch endlos diese zu konfigurieren bis meine private Cloud einsatzbereit ist. Ich will das herunterladen, starten, und dann muss das laufen. 

Wie nun die Lösung des ganzen lautet? Nextcloud! Und zwar schön verpackt als Docker Container. Wie das ganze installiert und konfiguriert wird (denn ganz ohne geht es dann doch nicht) zeige ich im folgenden Artikel.