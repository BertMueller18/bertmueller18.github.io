---
layout: post 
title:  "Upgrade your CA to SKP &amp; SHA256. Part II: Move from a CSP to KSP provider | StarWind Blog" 
date:   2017-02-17T21:37:23.732Z 
categories: pki sha256 windows certificate
link: https://www.starwindsoftware.com/blog/upgrade-your-ca-to-skp-sha256-part-ii-move-from-a-csp-to-ksp-provider 
tags:
  - links
ogtype: article 
---

> Upgrade your CA to SKP & SHA256. Part II: Move from a CSP to KSP provider
Posted by Didier Van Hoye on February 3, 2017	
Tags: backup, CA certificate, CSP, KSP, Microsoft Software Key Storage Provider, Microsoft Strong Cryptographic Provider, PKI, PowerShell, SCP, SHA256, vm
00000
				5/5
Move from a CSP to KSP provider

Once you have moved to a least Windows Server 2008 R2 you can take this step. Any version below doesn’t allow for this and should be considered the end of life. Many haven’t made the move from a CSP to KSP provider yet, even when they are already running Windows Server 2012 or 2012 R2 for a few reasons. There were some issues with older clients like Windows Server 2003 and Windows XP. These were fixed with a hotfix but in all seriousness, if you’re still on those OS versions you need to move a.s.a.p. and if not there’s nothing we can do to help you. A modern and secure PKI will be the last of your worries I’m afraid. For a Microsoft reference, see Migrating a Certification Authority Key from a Cryptographic Service Provider (CSP) to a Key Storage Provider (KSP).

