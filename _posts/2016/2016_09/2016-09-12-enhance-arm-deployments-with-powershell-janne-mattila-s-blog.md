---
layout: post
published: true
title: "Enhance ARM deployments with PowerShell – Janne Mattila's blog"
date: 2016-09-12T11:09:55.177Z
categories: azurerm deployment powershell 
link: https://blogs.msdn.microsoft.com/jannemattila/2016/08/26/enhance-arm-deployments-with-powershell/
tags:
  - links
ogtype: article
bodyclass: post
---

> Enhance ARM deployments with PowerShell
★★★★★★★★★★★★★★★
Janne MattilaAugust 26, 20160
0
0
0
Disclaimer: Cloud is very fast moving target. It means that by the time you’re reading this post everything described here could have been changed completely . Hopefully some things still apply to you! Enjoy the ride!

Azure Resource Manager templates (ARM) is excellent way to deploy your infrastructure to Azure (see example from my previous blog post to get started). However sometimes it might feel a bit of static when you need to build infrastructure that uses some shared elements or something that needs to be injected at runtime to the deployment.

But no worries PowerShell comes to the rescue! And by that I mean that we need to leverage scripting capabilities of PowerShell in our deployment pipeline. We’re not going to be in using pure static ARM templates and we’re not going to be using pure PowerShell either in our deployment but instead we want to pick best of both worlds. This lets us to get dynamic scripting characteristics to our deployment.

One very common scenario which people first bump into is the use of Key Vault in deployments. You of course want to securely manage your app secrets (source control is big no-no ) but it’s a bit of challenge to manage it. If you look at the Quick start ARM templates on GitHub or documentation about Key Vault (example one) you get instructed to use Key Vault as static reference which will not work in practice when you need to work with real multi-environment systems. Those static references of course work when you have single simple environment but when you want to deploy this to n environments then it’s not going to scale. And this is the part where I’ll use PowerShell magic to make it multi-environment friendly.
