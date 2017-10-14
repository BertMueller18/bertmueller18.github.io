---
layout: post 
title:  "Encrypting Data with PowerShell Cmdlets -- Microsoft Certified Professional Magazine Online" 
date:   2017-10-14T14:32:48.247Z 
categories: powershell certificate pki programming
link: https://mcpmag.com/Articles/2017/10/05/Encrypting-Data-with-PowerShell-Cmdlets.aspx 
tags:
  - links
ogtype: article 
---

> Encrypting Data with PowerShell Cmdlets
Here are three commands you can use to encrypt and decrypt data.

By Boe Prox10/05/2017
Encrypting data in today's day and age is pretty important if you want to keep things secret without the threat of someone else viewing things such as passwords, personably identifiable information or some other piece of data that you don't want to have openly available in clear text. Of course, if someone wants to get your data and has enough time and resources, they will find a way to get it. But we can certainly make it more challenging by encrypting the data using the cmdlets available in PowerShell V5.

There are three commands which make up the Cryptographic Message System (CMS) set of cmdlets that you can use to encrypt and decrypt data. These cmdlets make use of a public key cryptography where there is a public key (which you use for the encryption) and a private key (which is used for the decryption). The public key, as the name implies, can be given out to allow others to encrypt the data but the private key is something that you want to keep a tight hold on. If someone whom you do not trust gains access to this private key, they can use it to decrypt all of your data.  If you want to enjoy some light reading, you can read up on the CMS RFC here.

The three cmdlets which are available to use are Protect-CMSMessage, UnProtect-CMSMessage and Get-CMSMessage. Protect-CMSMessage is what you will use to encrypt the data which would then be saved to a file and can only be decrypted using the UnProtect-CMSMessage cmdlet. Using Get-CMSMessage, you can view more data about the encrypted document such as who can decrypt it.