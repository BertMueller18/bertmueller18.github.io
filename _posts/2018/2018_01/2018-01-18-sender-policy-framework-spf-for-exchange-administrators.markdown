---
layout: post 
title:  "Sender Policy Framework (SPF) for Exchange Administrators" 
date:   2018-01-18T22:04:58.819Z 
categories: exchange security spf dns
link: https://practical365.com/exchange-server/a-sender-policy-framework-spf-primer-for-exchange-administrators/ 
tags:
  - links
ogtype: article 
---

## A Sender Policy Framework (SPF) Primer for Exchange Administrators
DECEMBER 7, 2015 BY PAUL CUNNINGHAM 21 COMMENTS

Email spam continues to be a huge problem for organizations these days, and it usually falls on the Exchange administrator to do something about it. Aside from the usual anti-spam measures we can put in place to protect our own servers from spam, we also need to consider how to prevent spammers from spoofing (imitating) the domain names for our own organization. After all, it can be very embarrassing or cause serious brand damage to have spam and malware that uses your domain name.

To detect spoofed email many receiving servers, particularly those operated by large email providers such as Microsoft, Yahoo, Google, and AOL, will perform a check of the Sender Policy Framework (SPF) record for the sender’s domain when a sending server is attempting to send an email message.