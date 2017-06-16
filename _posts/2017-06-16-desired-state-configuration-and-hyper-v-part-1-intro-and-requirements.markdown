---
layout: post 
title:  "Desired State Configuration and Hyper-V – Part 1 - Intro and Requirements" 
date:   2017-06-16T19:42:50.526Z 
categories: powershell programming psdsc
link: http://www.altaro.com/hyper-v/desired-state-configuration-hyper-v-part-1-intro-requirements/ 
tags:
  - links
ogtype: article 
---

> Desired State Configuration and Hyper-V – Part 1 – Intro and Requirements
22 Jul 2014 by Andy Syrewicze    0     Hyper-V & PowerShell
13
Rate this (3 Votes)
 
Back in May, some will remember a follow-up post I wrote in regards to Microsoft’s Teched 2014 conference. One of the key items that was touted and revisited time and time again throughout the conference was Desired State Configuration, or DSC for short.

I remember attending one of several sessions on this groundbreaking technology, and one quote really stood out to me. The quote read something along the lines of: “DSC was the end game in mind when we (Microsoft) set out to create PowerShell”. If you think about that concept, it really makes sense that DSC’s functionality stems from PowerShell itself.

PowerShell already contains all the nuts and bolts required to make overarching configuration changes to entire systems, why can’t that functionality be leveraged on an ongoing basis to maintain configuration compliance for critical workloads.

This is exactly what DSC sets out to do.