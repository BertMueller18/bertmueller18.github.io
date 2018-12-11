---
layout: post 
title:  "Configuring an HTTPS Pull Server for Desired State Configuration" 
date:   2018-12-11T21:52:44.076Z 
categories: psdsc powershell
link: http://duffney.io/Configure-HTTPS-DSC-PullServer 
tags:
  - links
ogtype: article 
---

> Configuring an HTTPS Pull Server for Desired State Configuration
Applies to: Windows PowerShell 4.0, Windows PowerShell 5.0
This blog post will guide you through the process of setting up and configuring an HTTPS Pull Server to deploy Desired State Configurations to nodes. It will also walk you through the process of requesting the cert from the CA (Certificate Authority)! That is the main reason I’m taking the time to write the post, almost all the DSC training I’ve watched skips that step and leaves the viewer clueless on how to configure HTTPS since a cert is kind of a requirement. There are however some requirements for this blog post, most of which I’ve written about previously and I’ll link them below.