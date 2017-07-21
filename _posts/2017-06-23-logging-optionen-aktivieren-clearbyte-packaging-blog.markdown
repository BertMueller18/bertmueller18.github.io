---
layout: post 
title:  "Logging Optionen aktivieren | clearByte Packaging Blog" 
date:   2017-06-23T19:55:38.497Z 
categories: MSI deployment
link: http://blog.clearbyte.ch/logging-option-aktivieren/ 
tags:
  - links
ogtype: article 
---

## LOGGING OPTIONEN AKTIVIEREN
Dezember 2015 | Edgar Frei

Manchmal kann es hilfreich sein, wenn die globalen Logging Optionen Windows Installer auf dem Client aktiviert sind.
Um diese zu aktivieren, muss folgender Registry Key erstellt werden:


HKLM\SOFTWARE\Policies\Microsoft\Windows\Installer\Logging voicewarmup
Logfiles werden danach automatisch in %temp% abgelegt.

Beschreibung der Parameter:

v – Verbose output
o – Out-of-disk-space messages
i – Status messages
c – Initial UI parameters
e – All error messages
w – Non-fatal warnings
a – Start up of actions
r – Action-specific records
m – Out-of-memory or fatal exit information
u – User requests
p – Terminal properties
+ – Append to existing file
! – Flush each line to the log
