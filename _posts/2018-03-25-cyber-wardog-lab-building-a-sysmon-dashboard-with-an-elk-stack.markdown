---
layout: post 
title:  "Cyber Wardog Lab: Building a Sysmon Dashboard with an ELK Stack" 
date:   2018-03-25T15:51:31.072Z 
categories: elkstack sysmon
link: https://cyberwardog.blogspot.de/2017/03/building-sysmon-dashboard-with-elk-stack.html 
tags:
  - links
ogtype: article 
---

> Building a Sysmon Dashboard with an ELK Stack






















Threat Hunting is FINALLY a hot topic, and in the past couple of months the security community has been sharing amazing resources on how to hunt with the help of open source tools. One in particular that has got a lot of attention for endpoint visibility has been Sysmon, and with its latest capabilities added in version 6, hunting even for named pipe pivoting has become easier.

A few projects that I have read recently are awesome, and I highly recommend to take a look at them:

Graylog App - Sysmon Threat Intelligence Configuration
Back to Basics - Enhance Windows Security with Sysmon and Graylog
Sysmon - DFIR
Sysmon Hunter


Some of the things that I love about most the projects out there are the different ways how sysmon configs are being put together and how data is being consolidated and presented for hunting campaigns. Therefore, in this post, I will show you how you can also create your own Sysmon dashboard but with the help of an ELK stack. This will help you to tune your initial Sysmon configurations and get a good overview of what you can see and hunt for in your lab. If you haven't yet read my previous series "Setting up a Pentesting... I mean, a Threat Hunting Lab", I recommend you to do it before continuing reading (At least, for the purpose of this post, read and follow the steps in Part 5 & Part 6 in order to be ready to build your dashboard)