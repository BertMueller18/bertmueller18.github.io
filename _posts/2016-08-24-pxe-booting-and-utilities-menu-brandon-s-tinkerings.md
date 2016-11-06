---
layout: post 
published: true 
title: "PXE Booting and Utilities Menu - Brandon's Tinkerings" 
date: 2016-08-24T06:13:26.558Z 
link: http://brandon.penglase.net/index.php?title=PXE_Booting_and_Utilities_Menu 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Intro

PXE (Preboot Execution Environment) Booting, or just Network booting in general is very interesting, at least to me, and a few others. As I believe it was Marty Connor in this awesome video "gPXE: Modern FOSS Network Booting" said that some people get really excited over booting machines over networks (including the Internet!) while others... not so much.

Well, I'm one of those people who gets really excited over the idea of booting machines over a network, and I can't really put my finger on why, it's just awesome to me.

So, I wanted to document the netboot setups that I use at my home, and my work. This entry consists of my home network. My work one, I'll put in another entry (as it's significantly different in it's programming, but does the same functions), and link here.

Now, network booting isn't for everyone, and it doesn't fit every situation, so your mileage will vary greatly.

My home network consists of iPXE, PHP scripting, and separate utilities. All of this is detailed below... so lets begin!