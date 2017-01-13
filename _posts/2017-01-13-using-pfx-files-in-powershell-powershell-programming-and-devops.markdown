---
layout: post 
title:  "Using PFX Files in PowerShell | PowerShell, Programming and DevOps" 
date:   2017-01-13T15:06:56.442Z 
categories: powershell programming
link: https://dscottraynsford.wordpress.com/2017/01/10/using-pfx-files-in-powershell/ 
tags:
  - links
ogtype: article 
---

> Using PFX Files in PowerShell

One of the things I’ve been working on lately is adding a new resource to the xCertificate DSC Resource module for exporting an certificate with (or without) the private key from the Windows Certificate Store as a .CER or .PFX file. The very insightful (and fellow DSC Resource maintainer) @JohanLjunggren has been giving some really great direction on this new resource.

One of these suggested features was to be able to identify if the certificate chain within a PFX file is different to the chain in the Windows Certificate Store. This is because a PFX file can contain not just a single certificate but the entire trust chain required by the certificate being exported.