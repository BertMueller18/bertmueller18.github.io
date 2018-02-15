---
layout: post 
title:  "Detecting Advanced Threats with Sysmon, WEF and ElasticSearch" 
date:   2018-02-07T19:22:36.311Z 
categories: wef logstash elasticsearch windows security
link: https://joshuadlewis.blogspot.de/2014/10/advanced-threat-detection-with-sysmon_74.html 
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
Event logs are not a silver bullet.  However, event logs can provide a tremendous amount of host telemetry data that can aid in the detection of an advanced adversary.  Very few organizations collect the right event logs from relevant devices, and even fewer organizations are able to action these event logs.  This article is designed to showcase a proof of concept architecture for detecting indicators of compromise through event logs.  