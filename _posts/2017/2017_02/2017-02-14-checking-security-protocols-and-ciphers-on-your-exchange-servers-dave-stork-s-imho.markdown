---
layout: post 
title:  "Checking security protocols and ciphers on your Exchange servers – Dave Stork's IMHO" 
date:   2017-02-14T12:46:21.363Z 
categories: iis security
link: https://dirteam.com/dave/2015/06/07/checking-security-protocols-and-ciphers-on-your-exchange-servers/ 
tags:
  - links
ogtype: article 
---

> Checking security protocols and ciphers on your Exchange servers

Microsoft states that Exchange 2010 and 2013 are secure out of the box. With this they mean that every traffic coming in and out of Exchange is one way or another encrypted. Whether this is web traffic or specific for SMTP. Even IMAP and POP are enabled with mandatory encryption (although the services are disabled by default).

However the 