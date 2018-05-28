---
layout: post 
title:  "ZFS (ZoL) Samba Share in einem LXC Container - Geekbundle.org" 
date:   2018-05-26T09:09:59.486Z 
categories: zfs linux samba security
link: https://www.geekbundle.org/zfs-zol-samba-share-in-einem-lxc-container/ 
tags:
  - links
ogtype: article 
---

> ZFS (ZoL) Samba Share in einem LXC Container
Veröffentlicht von Madic
Ich hab ein bisschen gebraucht um mein in einem LXC Container gemountetes ZFS (Zol – ZFS on Linux) Dataset per Samba mit Schreibrechten für einen Benutzer einzurichten…
Aber was waren jetzt die Ausschlaggebenden Dinge, die wirklich funktioniert haben? Es war eine Kombination aus ZFS Dataset und Samba Einstellungen.
Ein einfaches zfs set sharesmb=on wie unter Solaris geht leider wegen der fehlenden Gesamtintegration unter Linux nicht…