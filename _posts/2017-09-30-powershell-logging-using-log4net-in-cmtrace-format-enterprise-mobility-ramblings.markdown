---
layout: post 
title:  "PowerShell Logging using Log4Net in CMtrace format - Enterprise Mobility ramblings" 
date:   2017-09-30T09:07:58.591Z 
categories: powershell  deployment
link: http://www.oscc.be/powershell/Logging-in-PowerShell/ 
tags:
  - links
ogtype: article 
---

> PowerShell Logging using Log4Net in CMtrace format
This post goes wider than regular ConfigMgr stuff and is about adding logging to all your scripts.


Kim Oppalfens
EMS MVP for over a decade, focussing on Automation, Hybrid Identity, DevOps enthousiast and overall self-proclaimed nice guy.

 Belgium / Malta
 Email
 Twitter
 LinkedIn
 Github
Subscribe to the EMS newsletter

Email Address

First Name

Last Name


This post goes wider than regular ConfigMgr stuff and is about adding logging to all your scripts.

Intro

As a ConfigMgr admin I’ve always been blessed to be working with a system that has extensive logging capabilities. A lot of my knowledge and troubleshooting skills, as a result, come from reading logfiles.

A while back, after writing yet another script, that could use decent logging. I set forward to find an easy way to add logging from the start of writing a new script. After some investigation I found a very popular logging framework from the .Net community called Log4Net https://logging.apache.org/log4net/index.html

