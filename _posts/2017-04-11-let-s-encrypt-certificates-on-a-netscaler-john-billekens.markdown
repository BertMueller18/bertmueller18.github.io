---
layout: post 
title:  "Let’s Encrypt Certificates on a NetScaler | John Billekens" 
date:   2017-04-11T20:54:00.761Z 
categories: netscaler reverseproxy letsencrypt
link: https://blog.j81.nl/2017/04/06/lets-encrypt-certificates-on-a-netscaler/ 
tags:
  - links
ogtype: article 
---

Let’s Encrypt Certificates on a NetScaler   Recently updated !
This entry was posted in Citrix Let's Encrypt Netscaler  and tagged Certificates Citrix Let's Encrypt NetScaler PowerShell  on 2017-04-06 by John Billekens
For a while now it’s possible to use Let’s Encrypt certificates, they are trusted (cross signed), secure and most of all FREE!

There are already a lot of tools available to generate these certificates. I haven’t come across a tool or script to generate these certificates and upload them to a Citrix NetScaler. So I thought why not build it myself. I already tried it in a previous attempt, but I wanted more automation and thus I created this version.