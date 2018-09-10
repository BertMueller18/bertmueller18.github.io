---
layout: post 
title:  "NetScaler Gateway in einer Multi-Domänen Umgebung | Thomas Krampe" 
date:   2018-09-10T11:00:25.600Z 
categories: netscaler networking 
link: https://thomas-krampe.com/2018/03/netscaler-gateway-in-einer-multi-domaenen-umgebung/ 
tags:
  - links
ogtype: article 
---

> NetScaler Gateway in einer Multi-Domänen Umgebung

Ein NetScaler Gateway für eine XenApp / XenDesktop Umgebung zu konfigurieren stellt sicherlich (auch Dank des Wizards) für die meisten kein Problem dar. Wie verhält es sich allerdings, wenn sich an dem Gateway auch Benutzer anderer Domänen anmelden sollen. Die einfache Lösung ist hier die Verwendung des UPN sowie entsprechende Authentifizierungsrichtlinien am Gateway.

In meinem speziellen Fall ist das leider keine Lösung, da die Benutzer oftmals den UPN nicht kennen (er unterscheidet sich leider von der E-Mail Adresse) und sie sind einfach den SAMAccountName gewohnt. Der ideale Weg wäre hier also den SAM Account zu verwenden.

Um das jetzt für den Benutzer möglichst einfach zu gestalten, wäre ein Domänen Drop-Down Feld auf der Anmeldeseite des Gateways in diesem Fall die einfachste Lösung.