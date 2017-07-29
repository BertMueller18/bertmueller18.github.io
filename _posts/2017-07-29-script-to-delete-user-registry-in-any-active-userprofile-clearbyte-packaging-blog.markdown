---
layout: post 
title:  "Script to delete user registry in any active userprofile | clearByte Packaging Blog" 
date:   2017-07-29T21:26:31.979Z 
categories: powershell automation
link: http://blog.clearbyte.ch/script-to-delete-user-registry-in-any-active-userprofile/ 
tags:
  - links
ogtype: article 
---

> SCRIPT TO DELETE USER REGISTRY IN ANY ACTIVE USERPROFILE
November 2015 | Michael Busslinger

Es kommt immer wieder vor, dass Registry Key gelöscht werden müssen bevor eine Applikation sauber installiert werden kann. Die Gründe dafür sind vielfältig und reichen von Lizenzierungs-anforderungen bis hin zu funktionalen Anforderungen.
Was bei HKLM Keys kein Problem ist, kann bei User Registry Keys zur Herausforderung werden. Aus diesem Grund haben wir das folgende Script erstellt, welches einen gewünschten Key aus allen vorhanden User Profilen löscht.

SID

Zuerst werden alle SID aus der Registry gelesen


1
objRegistry.EnumKey HKEY_USERS, "", arrSubkeys
Delete Key

Danach werden alle gefundenen SIDs nach dem zu löschenden Registry Key durchforstet. Wird dieser gefunden, erfolgt der Aufruf der Prozedur SearchAndDeleteSubkeys. Diese sorgt dafür, dass zuerst alle eventuell vorhandenen Subkeys gelöscht werden. Erst danach folgt das Löschen des Hauptkeys.