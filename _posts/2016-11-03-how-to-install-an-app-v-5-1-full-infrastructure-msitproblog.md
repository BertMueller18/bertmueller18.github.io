---
layout: post
published: true
title: "How to install an App-V 5.1 Full Infrastructure - msitproblog"
date: 2016-11-03T14:24:31.708Z
categories: appv app-v  
link: http://msitproblog.com/2015/10/27/installing-an-app-v-5-1-server-infrastructure/
tags:
  - links
ogtype: article
bodyclass: post
---

## How to install an App-V 5.1 Full Infrastructure Simon Dettling  27. October 2015  App-V  47 Comments
In this blog post I want to cover the setup of a new App-V 5.1 Server Infrastructure (Management- & Publishing-Server) from scratch. There are currently a few gotchas which I will cover, that can cause some Confusion if you don’t know them. Regarding the Management Database, I will perform the installation via the SQL Scripts instead of the native installer. The Advantage of this method is that you can use it to place the Management Database on a SQL Cluster.

Below you see a diagram of my servers in my lab environment.
