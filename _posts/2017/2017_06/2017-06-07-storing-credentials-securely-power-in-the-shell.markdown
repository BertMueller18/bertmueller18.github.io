---
layout: post 
title:  "Storing Credentials securely | Power in the shell" 
date:   2017-06-07T21:28:02.790Z 
categories: powershell programming certificate pki
link: https://powerintheshell.com/2017/05/11/storing-credentials-securely/ 
tags:
  - links
ogtype: article 
---

> Storing Credentials securely
Posted on 11. May 2017
Hi together,

I have been asked many times how to store and use securely credentials / passwords in scripts. The simplest thing is just to create a credential on a computer and export it via Export-Clixml where you make use of the SecureString and the native Windows Data Protection API (DAPI), which is secure. (take a look here) But the downside is that you can decrypt the securestring only at the computer and with the user who encrypted it.

Therefore I want to show you this simple but neat way to achieve this task on all computers. For this we simply make use of certificates to encrypt and decrypt the passwords which you would preferably create with your own PKI and deploy with your management solution.