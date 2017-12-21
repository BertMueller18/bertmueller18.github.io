---
layout: post 
title:  "The DOs and DON’Ts of PKI – Microsoft ADCS | Andrzej Kaźmierczak" 
date:   2017-11-15T07:22:52.303Z 
categories: activedirectory pki certificate 
link: http://kazmierczak.eu/itblog/2012/08/22/the-dos-and-donts-of-pki-microsoft-adcs/ 
tags:
  - links
ogtype: article 
---


## The DOs and DON’Ts of PKI – Microsoft ADCS

POSTED ON AUGUST 22, 2012 BY ANDRZEJ KAZMIERCZAK Share this post to your SOCIAL MEDIA!0

15
DON’T install PKI without a detailed plan. Ask yourself what you need it for, what features will you use and would it be scalable enough in the future.

DO use Windows Server Enterprise Edition for Active Directory users enrollment. UPDATE: This only applies to Windows Server 2008 R2 or earlier, as for Windows 2012 or later you can use Windows Server Standard Editions.

DO use a CAPolicy.inf file during installation. There you can define attributes such as basic constraints extension, renewal key length and period, CRLs period, etc.