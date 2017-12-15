---
layout: post 
title:  "Die Service Connection Points (SCPs) abfragen – @YusufsDirectoryBlog.onmicrosoft.com" 
date:   2017-11-15T07:28:02.198Z 
categories: activedirectory serviceconfigurationpoint scp
link: http://blog.dikmenoglu.de/2010/12/die-service-connection-points-scps-abfragen/ 
tags:
  - links
ogtype: article 
---

## Die Service Connection Points (SCPs) abfragen

Yusuf Dikmenoglu 5. Dezember 2010 0
Möchte man im Active Directory Informationen über einen Dienst der innerhalb einer Domäne zur Verfügung stehen soll veröffentlichen, so benötigt man ein Service Connection Point (SCP) Objekt. Ein SCP wird bei der Installation von vielen Applikation automatisch, ohne das Zutun des Administrators erstellt. Die SCPs gehören zur Klasse serviceConnectionPoint, die wiederum von der Klasse connectionPoint abgeleitet ist.