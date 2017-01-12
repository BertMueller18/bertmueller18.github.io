---
layout: post
published: true
title: "Citrix PVS: Optimize endpoint with PowerShell - Ingmar Verheij"
date: 2016-11-22T21:30:55.551Z
categories: pvs citrix powershell  
link: http://www.ingmarverheij.com/citrix-pvs-optimize-endpoint-with-powershell/
tags:
  - links
ogtype: article
bodyclass: post
---

> Citrix PVS: Optimize endpoint with PowerShell
WRITTEN BY INGMAR VERHEIJ ON JULY 24TH, 2013. POSTED IN POWERSHELL, PROVISIONING SERVER

With Citrix PVS the content of a disk is streamed over the network to an endpoint. This requires sufficient bandwidth and an optimized configuration. If both criteria are not met the endpoint suffers from delays, retries or failures.

A number of best practices apply when using Citrix PVS, most of them probably apply for your situation. In the past I had to optimize my VM’s manually each and every time I had to create a new vDisk! Ain’t nobody got time for that (link)!

I wrote a PowerShell script that optimizes the endpoint for Citrix PVS and would like to share it with you.
