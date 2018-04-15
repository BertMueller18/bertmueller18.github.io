---
layout: post 
title:  "How to create a Grafana metrics dashboard via Influx and PowerShell" 
date:   2018-04-15T13:10:55.736Z 
categories: powershell grafana 
link: http://wragg.io/windows-based-grafana-analytics-platform-via-influxdb-and-powershell/ 
tags:
  - links
ogtype: article 
---

> How to create a Grafana metrics dashboard via Influx and PowerShell
 21 Feb 2018


This blog post describes how you can use the open source tools Influx and Grafana along with a PowerShell module I've authored on Windows to create and populate interactive metric and monitoring dashboards like this one:



(-- note that all the graph labels and legends from the above screenshot have been removed to anonymize the data.)

I recently attended a DevOps meet up hosted by Shazam in their London office. The talks were held in a breakout area next to their open plan office space, through which were pillars covered in monitors displaying various Grafana dashboards. I hadn't seen Grafana before and this piqued my interest.

In case you're not aware, Grafana is an open source metrics dashboard and graph editor. It's power and popularity lies in the fact that it lets you put together beautiful looking dashboards with incredible ease that give you instant insight in to any metrics you wish to track (as well as allowing you to aggregate metrics from multiple sources).

Whether you are in development or operations or somewhere in between, you often want or need the ability to quickly and easily monitor something closely, be that a server, network or infrastructure metric or some component or behaviour of your application. Monitoring and measuring is a core tenet of DevOps.

