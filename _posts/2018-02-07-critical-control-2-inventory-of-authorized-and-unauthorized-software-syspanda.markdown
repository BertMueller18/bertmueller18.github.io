---
layout: post 
title:  "Critical Control # 2: Inventory of Authorized and Unauthorized Software - Syspanda" 
date:   2018-02-07T19:23:47.378Z 
categories: wef logstash elasticsearch kibana security windows
link: https://www.syspanda.com/index.php/2017/08/25/critical-control-2/ 
tags:
  - links
ogtype: article 
---

> Critical Control # 2: Inventory of Authorized and Unauthorized Software
by Pablo Delgado on August 25, 2017 in Security, security essentials
You can’t control what you can’t see
Do you have a list of approved and trusted applications in your environment? Are you sure? What about those 3rd party add-ons that users download or those ad-ware applications bundled in those PDF converters? The reality is that we might not be tracking all of our software entirely and especially those that are not authorized to run.

It’s a scary feeling not knowing what’s currently running on your systems and how those processes got there in the first place. The purpose of this article is to take advantage of existing resources to answer these questions. We will be leveraging Sysmon, Windows Event Forwarder, and Applocker (which is available for Windows Enterprise versions only).

There are commercial products out there that can easily discover your network and provide a list of software running such as Quest KACE 1000, or even Microsoft’s SCCM among others; they can easily be deployed through GPO and make your life easier.

For now, let’s do it the manual way and get to know our environment a little better.