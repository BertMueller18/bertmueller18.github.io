---
layout: post 
title:  "How to digitally sign PowerShell Scripts « SID-500" 
date:   2017-10-30T17:03:34.964Z 
categories: powershell programming security
link: https://sid-500.com/2017/10/26/how-to-digitally-sign-powershell-scripts/?utm_content=buffer703fe&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer 
tags:
  - links
ogtype: article 
---

> How to digitally sign PowerShell Scripts

In this article, a certificate for a digital signature is created to digitally sign files with Windows PowerShell. A digital certificate is usually issued by a Certification Authority (CA). But in this post, we are going to create a self-signed certificate. Of course with PowerShell. No need for 3rd party tools.


Introduction
A file is signed with a certificate. Cryptography can be used to verify authenticity. This is done using the key pair private key and public key. The file is digitally signed with the private key and the public key is used to verify its identity. The public key can be given to anyone. The private key is only yours. which means your identity can be verified.