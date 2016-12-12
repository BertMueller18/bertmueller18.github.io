---
layout: post 
title:  "	Deployment Research &gt; Research" 
date:   2016-12-12T21:58:55.165Z 
categories: deployment vmware powershell mdt
tags:
  - links
ogtype: article 
---

> Creating Reference Images using the VMware platform - Image Factory script by Johnny Radeck

Deployment Research
Johan Arwidmark

On this blog I previously posted PowerShell scripts to automatically generate reference images via the Hyper-V platform, often referred to as an Image Factory. Here is an example for the VMware platform, provided by my good friend Johnny Radeck. Thanks Johnny!

Note: This script can also be used as a base to create virtual machines for the hydration kits I have released, which are used for automating setup of entire lab environments. While the hydration kits work on any virtual platform that supports booting from an ISO file (meaning all of them), I only provided PowerShell scripts to create VMs for the Hyper-V platform. This script, with some modifications, can be used for that as well.