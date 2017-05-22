---
layout: post 
title:  "Exchange 2013/2010: Postfach-Back-up per PST-Export (PowerShell)" 
date:   2017-05-22T07:34:07.539Z 
categories: exchange powershell exchange2010 exchange2013
link: https://www.codetwo.de/blog/exchange-20132010-postfach-back-up-per-pst-export-powershell/5074 
tags:
  - links
ogtype: article 
---

> Exchange 2013/2010: Postfach-Back-up per PST-Export (PowerShell)
Posted on 14. März 2015
by Jarek Bednarz
Eine funktionierende E-Mail-Organisation geht zwangsweise mit effizientem Postfach-Back-up einher. Dennoch bieten alle bisherigen Versionen von Microsoft Exchange, Exchange 2013 miteingeschlossen, nur eingeschränkte Möglichkeiten für eine Brick-level-Sicherung. Im Grunde kann granulares Back-up nur mittels PST-Export bewerkstelligt werden. Diesen erledigt man entweder via Outlook oder PowerShell oder u.U. auch via Exchange Management Console / Control Panel. Im weiteren Teil des Beitrags widmen wir uns dem Weg über die PowerShell, und zwar am Beispiel von Exchange 2013 und Exchange 2010.