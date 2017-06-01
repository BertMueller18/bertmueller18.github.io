---
layout: post 
title:  "„Senden Als“ und „Senden im Auftrag von“ in Exchange 2010 | Education Support Centre Deutschland GmbH" 
date:   2017-06-01T22:17:47.455Z 
categories: exchange exchange2010 
link: https://www.escde.net/senden-als-und-senden-im-auftrag-von-in-exchange-2010/ 
tags:
  - links
ogtype: article 
---

> Senden Als“ und „Senden im Auftrag von“ in Exchange 2010
Posted on22. Mai 2013AuthorEileen Gröne3 Comments

In Exchange 2010 ist es sehr einfach Benutzern das Recht zu geben, für eine andere Mailbox E-Mails zu senden. Zum einen gibt es hierfür „Senden als“, mit dem die E-Mails so aussehen, also würden sie vom Eigentümer der Mailbox selbst kommen. Zum anderen gibt es aber auch „Senden im Auftrag von“, bei der der Empfänger klar erkennen kann, dass die E-Mail von Sender A im Auftrag von Benutzer B gesendet wurde.
Über die Exchange Management Shell können die Berechtigungen wie folgt vergeben werden:

Add-ADPermission BenutzerB -User BenutzerA -Extendedrights „Send As“

Set-Mailbox BenutzerB -GrantSendonBehalfTo BenutzerA