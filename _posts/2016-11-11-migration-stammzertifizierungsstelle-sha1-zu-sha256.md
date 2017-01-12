---
layout: post
published: true
title: "Migration Stammzertifizierungsstelle SHA1 zu SHA256"
date: 2016-11-11T08:21:09.979Z
categories: pki certificate windows 
link: https://www.frankysweb.de/migration-stammzertifizierungsstelle-sha1-zu-sha256-hashalgorithmus/
tags:
  - links
ogtype: article
bodyclass: post
---

## Migration Stammzertifizierungsstelle SHA1 zu SHA256 (Hashalgorithmus)
Veröffentlicht am20. März 2015AutorFrank14 Kommentare

Ab dem 01.01.2016 wird Microsoft SSL Zertifikate mit SHA1 als Hashalgorithmus für ungültig erklären. Webserver oder Dienste die Zertifikate mit SHA1 nutzen, lösen also Zertifikatswarnungen im Browser bei den Benutzern aus. Daher sollte langsam aber sicher damit begonnen werden, SHA1 Zertifikate auszutauschen. Damit eine interne CA Zertifikate mit SHA256 (SHA2) ausstellen kann, muss die CA von SHA1 auf SHA2 umgestellt werden. Hier gibt es das entsprechende Howto:

Hier sieht man das der Hashalgorithmus der CA auf SHA1 steht. Die CA kann somit auch nur Zertifikate mit SHA1 ausstellen.
