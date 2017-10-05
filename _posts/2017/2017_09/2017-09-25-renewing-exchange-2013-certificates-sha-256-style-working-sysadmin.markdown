---
layout: post 
title:  "Renewing Exchange 2013 Certificates: SHA-256 Style – Working Sysadmin" 
date:   2017-09-25T20:04:46.719Z 
categories: exchange certificate sha2 sha256 exchange2013 
link: http://www.workingsysadmin.com/renewing-exchange-2013-certificates-sha-256-style/ 
tags:
  - links
ogtype: article 
---

## Renewing Exchange 2013 Certificates: SHA-256 Style
January 14, 2015Exchange, PKI, Windows CAexchange, pki, windows ca
I recently ran into an issue that I think is actually pretty funny. It was time to renew the publicly trusted certificate that we install on our Exchange 2013 servers that gets tied to SMTP, OWA and some other IIS services like autodiscover. Since SHA-1 is on the road to deprecation, our cert vendor pushed pretty hard to get something with a hashing algorithm of SHA-2 (or SHA-256, it’s the same thing). Sounds reasonable, right?

Well, here’s the problem. Even though Microsoft is one of many vendors who is pushing the deprecation of SHA-1, Exchange 2013 doesn’t seem to have a mechanism built into it that generates a SHA-2 cert request. Even the New-ExchangeCertificate PowerShell command doesn’t have a way to change which hashing algorithm is used. Windows 2008 R2 and later support SHA-2 but at the time of writing this article, Exchange 2013 doesn’t have a way to generate such a request.

There are other ways to generate cert requests, though. Since Windows Server 2012 R2 supports SHA-2, and even SHA-2 certificates, perhaps – I thought – the Certificates MMC can be used to generate such a cert. I was right, it can be used to generate a SHA-2 cert. “Great!” I can hear you exclaim, “Now give me the steps on how to do it!” Not so fast. I’m not going to put the full steps to generating a SHA-2 certificate using the Windows Certificates MMC here because of a problem.

To generate a SHA-2 request using the Certificates MMC, you add the Certificates for Local Computer snapin to MMC.exe, right click on the Personal certificate store and generate a new request. When asked to choose a request template, you are offered two choices: Legacy or CNG. Legacy doesn’t support changing your hashing algorithm and therefore only generates SHA-1 requests. CNG it is, then! I continued on, generated my SHA-2 cert request, got it approved and took the certificate from my provider and went to test it. Almost everything worked except I couldn’t log into OWA or ECP. Why not? Because Exchange 2013 stores lots of info in encrypted cookies about you when you log into these services and it can’t use a CNG certificate to decrypt the data. Whenever I logged in, I would be immediately redirected back to the login page as if nothing had happened because the encrypted cookie with all my info (like “you logged in as username“) couldn’t be decrypted since Exchange 2013 can’t use the CNG provider in Windows 2012 R2.

How else can you generate a SHA-2 certificate request, then? The Windows MMC requires you to associate it with a CNG provider that Exchange 2013 can’t use and Exchange 2013 doesn’t allow you to create a SHA-2 request? This isn’t looking good, SHA-1 is being deprecated and I have to renew my certificate!

The answer turns out to be unbelievably easy. I couldn’t believe this worked.

Here’s the answer. Here’s how to renew your Exchange 2013 public certificate with a SHA-2 hashing algorithm…

Use the New-ExchangeCertificate PowerShell command to generate a cert request that is perfect for your needs, minus the fact that it will request a SHA-1 hashing algorithm.
Submit the request to your public certificate provider but indicate that it is a SHA-2 certificate request. Your provider should have an option to indicate what sort of certificate your request is set up for. Make sure you say SHA-2.
Your provider will give you back a SHA-2 certificate that is not associated with a CNG provider that will work with your Exchange 2013 environment for all SMTP, IIS, IMAP and POP services you wish to bind it to.
That’s right, the answer is to generate a SHA-1 request anyway and tell your provider that it’s SHA-2.