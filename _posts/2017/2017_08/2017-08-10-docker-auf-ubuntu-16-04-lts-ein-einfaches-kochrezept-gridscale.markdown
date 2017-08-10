---
layout: post 
title:  "Docker auf Ubuntu 16.04 LTS - ein einfaches Kochrezept - gridscale" 
date:   2017-08-10T07:44:32.601Z 
categories: linux docker ubuntu
link: https://gridscale.io/community/tutorials/docker-ubuntu/ 
tags:
  - links
ogtype: article 
---

> Docker auf Ubuntu 16.04 LTS – ein einfaches Kochrezept
vom gridscale Team Docker Ubuntu

Um was geht es bei Docker?
Bei Docker handelt es sich um eine Open-Source-Software zur “Anwendungsverteilung”. Klingt erst einmal Abstrakt. Fand ich vor einiger Zeit auch und habe dann angefangen mich genauer mit Docker zu befassen. Jetzt möchte ich dir Docker gerne in diesem ersten Artikel näher bringen und dich bei deinen ersten Schritten mit Docker begleiten. Dieser Blogbeitrag richtet sich an Anwender, die ihre ersten Schritte mit Docker machen möchten und beleuchtet nur grundlegende Dinge. Es folgen weitere Beiträge, die etwas tiefer einsteigen. Mehr dazu später.

Wenn du Verbesserungsvorschläge zu diesem Artikel hast, dann freue ich mich sehr über einen kurzen Kommentar oder Hinweis. Du erreichst das Team von gridscale jederzeit unter team@gridscale.io.

Bevor wir loslegen, drei wichtige Begriffe:

Image: ein fertiger Docker-Container, den du einfach von einem Host zum nächsten Host portieren oder dublizieren kannst.
Container: ein virtuelles Betriebssystem, bereit für die Aufnahme einer Docker-Anwendung.
Dockerfile: eine Sammlung an Befehlen und Parametern, um ein bestehendes Image an die eigenen Bedürfnisse anzupassen. Beispielsweise Änderung von Kennwörtern, konfigurieren von Domains, etc…
Diesen Artikel baue ich auf einem Ubuntu 16.04 LTS auf, du kannst aber auch andere Distributionen verwenden. Wenn es an irgendeiner Stelle hakt, schreib uns kurz an, dann helfen wir dir gerne weiter