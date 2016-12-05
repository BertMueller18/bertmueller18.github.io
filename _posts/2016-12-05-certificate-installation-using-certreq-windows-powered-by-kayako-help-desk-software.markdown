---
layout: post 
title:  "Certificate Installation: Using certreq (Windows) - Powered by Kayako Help Desk Software" 
date:   2016-12-05T10:03:16.098Z 
categories: pki certificate certreq
link: https://support.comodo.com/index.php?/Default/Knowledgebase/Article/View/814/37/ 
tags:
  - links
ogtype: article 
---

> 
Certificate Installation: Using certreq (Windows)
This article is for administrators who prefer the command shell!


When your certificate is issued you'll typically receive a file called store_acmesave_com.cer. Save it on the server and from the same directory run:

certreq -accept store_acmesafe_com.cer 