---
layout: post 
title:  "Sending Windows Event Logs to Logstash - /dev/random" 
date:   2018-02-07T19:25:21.935Z 
categories: eventlog logstash wef
link: https://blog.rootshell.be/2015/08/24/sending-windows-event-logs-to-logstash/ 
tags:
  - links
ogtype: article 
---

> Sending Windows Event Logs to Logstash
August 24, 2015 Forensics, Incident Management, PowerShell, Security 23 comments
This topic is not brand new, there exists plenty of solutions to forward Windows event logs to Logstash (OSSEC, Snare or NXlog amongst many others). They perform a decent job to collect events on running systems but they need to deploy extra piece of software on the target operating systems. For a specific case, I was looking for a solution to quickly transfer event logs from a live system without having to install extra software.


The latest versions of the Microsoft Windows come with Powershell installed by default. Powershell is, as defined by Wikipedia, a task automation and configuration management framework. PowerShell 3 introduced nice cmdlets to convert data from/to JSON which is a format natively supported by Logstash. The goal is to have a standalone Powershell script executed from a share or a read-only USB-stick that will process Windows event logs and send them to a remote preconfigured Logstash server on a specific TCP port.