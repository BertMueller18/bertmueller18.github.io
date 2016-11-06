---
layout: post 
published: true 
title: "Images anlegen qemu-img create, kvm-img dd iso raw qcow qcow2 Overlay ovl, sparse image, sparse files, genisoimage - qemu, kvm, xen &amp; libvirt" 
date: 2016-09-05T19:36:09.846Z 
link: http://qemu-buch.de/de/index.php?title=QEMU-KVM-Buch/_Speichermedien/_Images_anlegen#Overlay-Images_anlegen 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Images anlegen qemu-img create, kvm-img dd iso raw qcow qcow2 Overlay ovl, sparse image, sparse files, genisoimage
(Link zu dieser Seite als [[QEMU-KVM-Buch/ Speichermedien/ Images anlegen]])
<<<|###| >>> | English

Inhaltsverzeichnis [Verbergen]
1 Images anlegen
1.1 Anlegen von Images mit qemu-img
1.2 Anlegen von raw-Images und Sparse-Dateien mit dd
1.3 Effektives Kopieren von Sparse-Dateien
1.4 Overlay-Images anlegen
1.5 Live-Snapshot eines Devices
1.6 CDs, DVDs und Disketten als Image importieren
1.7 Anlegen eines CD-Image aus einem Verzeichnis
1.8 Bearbeiten von CD/DVD-Images
[bearbeiten] Images anlegen
Virtuelle Maschinen nutzen meist Image-Dateien als virtuelle Speichermedien. Diese lassen sich auf andere Rechner übertragen und sind damit flexibler einsetzbar als die ebenfalls mögliche Nutzung realer Festplatten. Nach dem Anlegen müssen diese Image-Dateien, wie reale Speichermedien, partitioniert und formatiert werden. Dies kann durch Programme der Gast-Systeme geschehen.