---
layout: post 
title:  "Powershell und Zertifikate | clearByte Packaging Blog" 
date:   2017-07-29T21:25:16.009Z 
categories: powershell automation
link: http://blog.clearbyte.ch/powershell-und-zertifikate/ 
tags:
  - links
ogtype: article 
---

## POWERSHELL UND ZERTIFIKATE
Juli 2016 | Michael Busslinger

Mit PowerShell ist es ziemlich einfach Zertifikate zu installieren, zu entfernen und aufzulisten.
Dieses Beispiel zeigt die Installation, Deinstallation eines Zertifikats in den Root Certification Store.

### Zertifikat installieren

````powershell
Import-Certificate -FilePath '<pfad zum zertifikat>' -CertStoreLocation cert:\LocalMachine\Root -verbose
````
### Zertifikat entfernen

````powershell
Remove-Item -Path cert:\LocalMachine\Root\<certID> -verbose
````
### Zertifikate auflisten

Mittels Get-ChildItem können alle auf dem Client installierten Zertifikate aufgelistet werden.

````powershell
Get-ChildItem -Path Cert:\LocalMachine\Root | Out-GridView
````