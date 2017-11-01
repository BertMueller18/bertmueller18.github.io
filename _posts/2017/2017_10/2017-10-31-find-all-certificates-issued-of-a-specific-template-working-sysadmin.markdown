---
layout: post 
title:  "Find All Certificates Issued Of A Specific Template – Working Sysadmin" 
date:   2017-10-31T09:56:21.199Z 
categories: activedirectory pki certificate 
link: http://www.workingsysadmin.com/find-all-certificates-issued-of-a-specific-template/ 
tags:
  - links
ogtype: article 
---

> Find All Certificates Issued Of A Specific Template
March 4, 2015PKI, PowerShell, PowerShell ISEpki, powershell, powershell ise
As part of another PowerShell script I’m writing, I needed to get an array of all of the certificates issued in my Enterprise PKI environment by a specific Issuing Certificate Authority (CA) that are of a certain Certificate Template.That doesn’t sound like such a tall order. You can launch MMC.exe, add the Certification Authority module, browse the issued certificates and see for yourself the different issued certs and their template.

PowerShell is a bit trickier, though, for a couple reasons. First, you’re going to need a PowerShell module to help you with this task. I really like PSPKI (available on CodePlex). Install that module and run the command to import the module.