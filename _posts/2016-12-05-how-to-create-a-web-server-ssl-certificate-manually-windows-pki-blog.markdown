---
layout: post 
title:  "How to create a web server SSL certificate manually – Windows PKI blog" 
date:   2016-12-05T10:05:24.480Z 
categories: pki certificate certreq
link: https://blogs.technet.microsoft.com/pki/2009/08/05/how-to-create-a-web-server-ssl-certificate-manually/ 
tags:
  - links
ogtype: article 
---

#How to create a web server SSL certificate manually

The Internet Information Server (IIS) and Microsoft Internet Security and Acceleration (ISA) provide wizards in the administration user interface to request and install SSL certificates. With this blog post I want to explain how to request a SSL server certificate manually. The manual steps are required if the Certification Authority (CA) is not available in the same forest as the IIS or ISA is a member of.