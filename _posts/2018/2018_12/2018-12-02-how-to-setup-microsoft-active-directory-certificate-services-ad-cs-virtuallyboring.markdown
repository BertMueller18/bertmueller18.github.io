---
layout: post 
title:  "How to setup Microsoft Active Directory Certificate Services [AD CS] - VirtuallyBoring" 
date:   2018-12-02T22:45:31.374Z 
categories: pki certificates security windows activedirectory
link: https://www.virtuallyboring.com/setup-microsoft-active-directory-certificate-services-ad-cs/ 
tags:
  - links
ogtype: article 
---

> How to setup Microsoft Active Directory Certificate Services [AD CS]
March 15, 2016 by Daniel
Microsoft Active Directory Certificate Services [AD CS] provides a platform for issuing and managing public key infrastructure [PKI] certificates. On top of securing application and HTTP traffic the certificates that AD CS provides can be used for authentication of computer, user, or device accounts on a network.

In this post I will be setting up a single AD CS server on my domain and configuring group policy to auto enroll my servers. For an enterprise environment you will deploy subordinate CA’s and shut down your root CA for security. For more information about this setup click here: PKI Design Options