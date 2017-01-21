---
layout: post 
published: true 
title: "Storefront+Receiver speichern von Passwörtern ermöglichen bei verschiedenen Domänen – How-To-Compute" 
date: 2016-08-29T04:20:07.685Z 
categories: citrix storefront activedirectory sso
link: http://www.how-to-compute.de/2014/08/18/storefrontreceiver-speichern-von-passwoertern-ermoeglichen-bei-verschiedenen-domaenen/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Storefront+Receiver speichern von Passwörtern ermöglichen bei verschiedenen Domänen
Marcel Strohmeyer 18/08/2014 Citrix, Storefront, Windows Desktop OS, XenApp, XenApp6.5 Comments
Hallo zusammen,
ich hatte letztens die Anfrage von einem Kunden das er gerne seine Passwörter im Receiver speichern möchte, dies aber in Verbindung mit Storefront + anderer Domäne in der der Storefront steht nicht hin bekommen hat.
Es war einfach keine Möglichkeit am Receiver gegeben den Harken zu setzen „Save Passwort“

Nach Recerche kam ich auf folgenden Registry Eintrag:



Dieser kann mit folgenden Werten bestückt werden:



In meinem Fall war „A“ der richtige Eintrag.

Original Citrix Artikel ist dieser hier:

http://support.citrix.com/article/CTX134341
