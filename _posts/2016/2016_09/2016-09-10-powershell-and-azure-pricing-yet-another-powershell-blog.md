---
layout: post
published: true
title: "Powershell and Azure pricing – Yet another PowerShell blog"
date: 2016-09-10T11:29:27.097Z
categories: powershell azure
link: https://eosfor.wordpress.com/2016/09/09/powershell-and-azure-pricing/
tags:
  - links
ogtype: article
bodyclass: post
---

## POWERSHELL AND AZURE PRICING

September 9, 2016eosfor
Sometimes it is difficult to calculate prices for Azure. Especially when you have a lot of machines. What to do? It is easy:

$request = Invoke-WebRequest -Uri https://azure.microsoft.com/api/v1/pricing/virtual-machines/calculator/?culture=en-us
$offers = $request.Content | ConvertFrom-Json
 
$offers.offers.'standard-d11v2'.prices | select -Property "us-east*"
Enjoy
