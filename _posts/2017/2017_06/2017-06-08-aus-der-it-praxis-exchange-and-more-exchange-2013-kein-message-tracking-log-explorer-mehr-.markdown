---
layout: post 
title:  "Aus der IT Praxis... Exchange and more: Exchange 2013: Kein Message Tracking Log Explorer mehr?" 
date:   2017-06-08T20:20:19.369Z 
categories: exchange exchange2013 messagetracking
link: http://it-blog.bru.ch/2013/06/exchange-2013-kein-message-tracking-log.html 
tags:
  - links
ogtype: article 
---

> Exchange 2013: Kein Message Tracking Log Explorer mehr?
Ein Tool, welches leider im Exchange 2013 nicht mehr vorhanden ist, ist der "Message Tracking Log Explorer". Neu soll das Message Tracking über die Weboberfläche gemacht werden.

Das Webbasierte Tool war mir noch nie sonderlich sympathisch. Unter Exchange 2013 ist es noch schlimmer geworden. Es ist nur noch möglich dem Exchange bekannte Postfächer, Mail-User oder Kontakte als Absender oder Empfänger in die Suchmaske einzugeben.

Wenn ich wissen will, ob meine Mail an einen externen Empfänger ausgeliefert werden konnte, muss die externe Mailadresse als Kontakt erfasst sein. Es gibt auch keine Möglichkeit einen Zeitrahmen anzugeben.

Also kurz gesagt: Das Tool ist für Exchange Administratoren nicht zu gebrauchen.

Wie sollen Exchange Admins also in Zukunft kontrollieren ob Mails angekommen oder versendet worden sind? Nach Meinung von Microsoft sollen wir dies anscheinend in der Exchange Shell erledigen. Dies ist ja in Ordnung, aber nicht besonders übersichtlich. Darum möchte ich hier ein paar Tricks posten, die das Tracking wieder etwas übersichtlicher machen.