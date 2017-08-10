---
layout: post 
title:  "Detecting Advanced Threats with Sysmon, WEF and ElasticSearch" 
date:   2017-02-10T14:14:57.861Z 
categories: pentest security incidentresponse elasticsearch
link: https://joshuadlewis.blogspot.de/2014/10/advanced-threat-detection-with-sysmon_74.html?m=1 
tags:
  - links
ogtype: article 
---

> Detecting Advanced Threats with Sysmon, WEF and ElasticSearch
Panther Detect
Author: Joshua Lewis
Post Date: October, 2014; Updated December 2015


Why event logs?
From an advanced threat detection perspective, most analysts are relatively blind at the host level until they receive network telemetry or a security agent alert (Anti-Virus/HIPS).  Based on my experience, network telemetry data is typically collected at network egress points and Anti-Virus/HIPS is poor at detecting pivot and memory based attacks.  One approach to overcome these obstacles is to increase visibility at the host level and create indicators of compromise that can trigger forensic investigation by alerting on specific event logs.  Event logs are built natively into most operating systems and can immediately send valuable artifacts to a log collector prior to the attacker having the ability to modify the integrity of the system.