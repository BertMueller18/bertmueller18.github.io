---
layout: post 
title:  "Self-signed certificate chain using OpenSSL X509 module" 
date:   2018-07-05T13:19:01.857Z 
categories: pki openssl certificate
link: https://thamizh85.github.io/notes/sysadmin/2017/08/20/self-signed-certificate-chain-using-openssl-x509-module/ 
tags:
  - links
ogtype: article 
---

## Self-signed certificate chain using OpenSSL X509 module
 Posted on 2017-08-20 |  In Notes , SysAdmin ,
Introduction
Generating a self-signed CA certificate or signing a web server certificate using openssl is very easy. There are tons of resources out there in the web. But creating a certificate, which works without any warning on most modern browsers is a challenge. This challenge is compounded by ever-growing stringent requirements from the popular browsers (See footnote 1).

There are two ways to use openssl to mimic a CA. The first option is to use ‘openssl ca’ module, for which there are many guides in the internet. This module mimics a full-fledged CA and useful when you are setting up something for long term requiring features such as CRL and OCSP.

The other option is to use ‘openssl x509’ module which is what we will be focusing on. I chose this because I just needed a certificate pair for one-off use and didn’t want to be bothered in setting up an elaborate CA configuration. The guide will be useful for someone with a similar objective.