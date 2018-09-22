---
layout: post 
title:  "Running the TICK Stack on Windows - DZone DevOps" 
date:   2018-09-20T06:29:37.426Z 
categories: grafana monitoring elasticsearch
link: https://dzone.com/articles/running-the-tick-stack-on-windows 
tags:
  - links
ogtype: article 
---

## Running the TICK Stack on Windows
Learn how to install and configure the TICK stack — Telegraf, InfluxDB, Chronograf, and Kapacitor — on Windows.
  by Noah Crowley     ·  May. 20, 18 · DevOps Zone · Tutorial

Every now and then we get requests from a developer using Windows, or a Windows-using participant at one of our workshops or events. Windows support is considered "experimental" for all components except Telegraf, but the full TICK Stack will still build and run on the platform, and we provide binaries for Windows on our downloads page. So while Windows is not an officially supported operating system and is not recommended in production, we wanted to provide some additional resources for those adventurous developers who still want to get up and running on the platform. This post will go over details of installation and configuration natively on Windows, and then touch briefly on some alternative approaches for running the TICK stack, such as Virtual Machines or Docker.

The following instructions were tested using Microsoft's Windows 10 Development Environment VMs.