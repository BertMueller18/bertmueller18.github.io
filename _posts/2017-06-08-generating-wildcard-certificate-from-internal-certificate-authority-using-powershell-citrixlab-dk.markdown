---
layout: post 
title:  "Generating wildcard certificate from internal certificate authority using PowerShell – Citrixlab.dk" 
date:   2017-06-07T22:07:45.062Z 
categories: powershell pki certificate 
link: http://citrixlab.dk/?p=544 
tags:
  - links
ogtype: article 
---

> When you are building Citrix environments or any other environment that uses certificates it is often easiest to use a wildcard certificate from your internal PKI infrastructure when you are testing. I had a talk with Dave Brett at Synergy about automating the process of getting a wildcard PFX certificate that can be used during automation of Citrix installations. I thought it would be an easy task since Microsoft has baking in PowerShell in most of their products and services now, but it turned out that I couldn’t find any native PowerShell commands that allowed be to perform the task.