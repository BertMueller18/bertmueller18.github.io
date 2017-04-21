---
layout: post 
title:  "Home Server Certfificate Management with XCA – MBSE Web" 
date:   2017-04-21T15:10:39.677Z 
categories: pki sha256 xca certificate 
link: http://www.mbse.eu/linux/homeserver/essential/certificatesxca/ 
tags:
  - links
ogtype: article 
---

## Home Server Certfificate Management with XCA
### Introduction.

A lot of server software needs certificate files to allow encrypted connections, think about mail TLS connections, https for safe web browsing etc. Large companies let these certificates sign or create by expensive companies so that they are valid in the usual chain of trusted certificates. For our Home Server this is too expensive and not needed. But we do need a complete chain to make our life a little bit easier.   If we create a complete chain including a CA (Central Authority) root certificate, then we only need to install that root certificate once on all our computers on our network.

In the early days of these articles I used scripts to create the certificates. You can find the old article here. But now I started using XCA which is a CA management program that runs in X-Windows. This program uses a database to store all the certificates, keys and structure. This database has a password but isn’t encrypted, so for better protection, store this database on an external disk like a SD card or USB stick and keep it in a safe place. You can encrypt this external drive.

In this article, I will describe how to create the root certificate and one server certificate for the mail server. All other certificates will be described with the articles where they belong to. We will also publish a certificate revoke list (crl), and put it on a public website. That same site is a good place to publish the public part of the root certificate too so that it is easy to download and install on client computers