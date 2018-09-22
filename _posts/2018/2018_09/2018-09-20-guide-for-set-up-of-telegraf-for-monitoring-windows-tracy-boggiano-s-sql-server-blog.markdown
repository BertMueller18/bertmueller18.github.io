---
layout: post 
title:  "Guide for Set Up of Telegraf for Monitoring Windows | Tracy Boggiano's SQL Server  Blog" 
date:   2018-09-20T07:14:10.323Z 
categories: grafana windows
link: https://tracyboggiano.com/archive/2018/04/guide-for-set-up-of-telegraf-for-monitoring-windows/ 
tags:
  - links
ogtype: article 
---

> Guide for Set Up of Telegraf for Monitoring Windows

Collecting Performance Metrics
Guide for Set Up of Telegraf for Monitoring SQL Server xPlat
Guide for Set Up of Telegraf for Monitoring Windows
Setting up Telegraf to Startup on Windows
Guide for Setting up Telegraf to Monitor InfluxDB
Problem
As good DBAs, we sometimes have the need to monitor stats or just want to be nice to our system admins and share our new shiny toys and watch Windows using the same tools as SQL Server.

Install and Configure Telegraf for on Windows
The solution for this is fairly simple now that you have setup Part 1 of this series.  You can download the Windows conf file for Telegraf from my presentation.  Below are the important pieces of the file. The main part of the OUTPUT PLUGINS being to place the data in the InfluxDB database. The data will be housed in the same database as our SQL performance metrics. Next, you can collect any Windows Performance Counters you want and group them into a “Measurement”. I’m using the dashboard that is on the Grafana website along with the performance metrics they have set up to be collected.