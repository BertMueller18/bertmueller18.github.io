---
layout: post 
title:  "Migrate Microsoft Certification Authority to SHA-2 Algorithm – My IT World" 
date:   2017-04-26T22:27:46.352Z 
categories: pki certificate sha256
link: http://myitworld.azurewebsites.net/2015/08/24/migrate-microsoft-certification-authority-sha-2-algorithm/ 
tags:
  - links
ogtype: article 
---

> MIGRATE MICROSOFT CERTIFICATION AUTHORITY TO SHA-2 ALGORITHM

 August 24, 2015  Arthur REMY Comments  1 Comment
TwitterLinkedInFacebookGoogle+
Microsoft is announcing a policy change to the Microsoft Root Certificate Program. The new policy will no longer allow root certificate authorities to issue X.509 certificates using the SHA-1 hashing algorithm for the purposes of SSL and code signing after January 1, 2016. Using the SHA-1 hashing algorithm in digital certificates could allow an attacker to spoof content, perform phishing attacks, or perform man-in-the-middle attacks.

Microsoft recommends that certificate authorities no longer sign newly generated certificates using the SHA-1 hashing algorithm and begin migrating to SHA-2. Microsoft also recommends that customers replace their SHA-1 certificates with SHA-2 certificates at the earliest opportunity.