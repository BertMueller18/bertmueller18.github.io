---
layout: post 
title:  "Creating Custom Windows Event Forwarding Logs – Practical Windows Security" 
date:   2018-02-07T19:41:45.598Z 
categories: wef security eventlog windows
link: https://blogs.technet.microsoft.com/russellt/2016/05/18/creating-custom-windows-event-forwarding-logs/ 
tags:
  - links
ogtype: article 
---

## Creating Custom Windows Event Forwarding Logs

You may have noticed recently that *we* Microsoft security people have kind of fallen in love with Windows Event Forwarding (WEF). Why? Its built into Windows itself, easily configurable and can collect a very large amount of course or finely filtered events (including existing events) from any domain joined machine with less then 30 minutes of effort.

When demonstrating WEF to customers, one of the most common questions I receive is "I don't want everything in Forwarded Events, can I create separate logs for my subscriptions?" The answer is yes, but it takes a little bit of effort. Once complete, you can create as many custom "buckets" for your forwarded events as you like. Let's start.

Firstly, a large amount of credit goes to Ted Hardy for providing the majority of the process for this. I'm really just playing technical writer here.

Before we start, you will need a few things.

If you don't have it already laying around, grab a copy of the Windows SDK for your OS. Why? We need to compile a .dll. I'm not a programmer and I don't understand what resource and link files are, but thankfully you don't really need to.
Right-click to download the template "manifest" file from this blog post and rename it to .man from .txt.
A machine to configure all of this on. I used a throw away virtual machine with Windows Server 2012 R2 and the Windows 8.1 SDK from above to perform these steps.