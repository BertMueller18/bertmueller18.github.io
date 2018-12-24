---
layout: post 
title:  "Autodiscover in an Exchange interorg migration with Quest QMM | Jaap Wesselius" 
date:   2018-12-06T14:20:41.929Z 
categories: exchange autodiscover
link: https://jaapwesselius.com/2018/11/29/autodiscover-in-an-exchange-interorg-migration-with-quest-qmm/ 
tags:
  - links
ogtype: article 
---

> AUTODISCOVER IN AN EXCHANGE INTERORG MIGRATION WITH QUEST QMM
NOVEMBER 29, 2018 JAAPWESSELIUS	2 COMMENTS
Outlook clients get their configuration information using the Autodiscover protocol from the Exchange server where their mailbox resides and the underlying Active Directory. This works fine, until you are in an interorg migration scenario using the Quest Migration Manager (QMM) for Exchange.

When using Microsoft tools (ADMT, Prepare-MoveRequest.ps1 and New-MoveRequest) the source Mailbox in Exchange is converted to a Mail-Enabled user at the moment of migration finalization. At the same moment the Mail-Enabled User property targetAddress is stamped with the SMTP address of the Mailbox in the new forest. SMTP works fine now, and also Autodiscover will follow the SMTP domain that’s in the targetAddress property. This is true for an interorg migration on-premises, but it is also true when moving Mailboxes from Exchange on-premises to Exchange Online in a hybrid scenario.