---
layout: post 
title:  "Powershell v5 Classes &amp; Concepts" 
date:   2017-03-03T06:50:48.024Z 
categories: powershell programming psdsc
link: https://xainey.github.io/2016/powershell-classes-and-concepts/ 
tags:
  - links
ogtype: article 
---

## Powershell v5 Classes & Concepts


Abstract
The release of Powershell WMF5 added classes to help simplify the creation of DSC resources. The class wrapper helps us encapsulate and localize variables and methods by creating objects. Classes expose an entirely new paradigm to Powershell known as Object-Oriented Programming. Taking a glance at the authoring process for earlier modules and DSC resources we can see a few common problems. Code duplication, an easily identifiable code smell, is found through many of the open source projects. Dynamic scoping and encapsulation issues forced developers to clear, cast, or rename variables. Many of these problems are easily resolved using OOP. The following article outlines the basic syntax of PowerShell classes while subsequently introducing intermediate and advanced design pattern concepts.