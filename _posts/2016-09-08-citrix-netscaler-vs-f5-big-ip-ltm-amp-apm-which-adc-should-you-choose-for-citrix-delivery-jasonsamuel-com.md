---
layout: post 
published: true 
title: "Citrix NetScaler vs F5 Big-IP LTM &amp; APM – Which ADC should you choose for Citrix delivery? – JasonSamuel.com" 
date: 2016-09-08T08:29:16.873Z 
link: http://www.jasonsamuel.com/2014/04/24/citrix-netscaler-vs-f5-big-ip-ltm-apm-which-adc-should-you-choose-for-citrix-delivery/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Citrix NetScaler vs F5 Big-IP LTM & APM – Which ADC should you choose for Citrix delivery?By Jason Samuel
onApril 24, 2014
1SHARESHARE TWEET SHARE SHARE 2 COMMENTS


NetScalers are my favorite Citrix product hands down. But I like to be well rounded and play with all technologies if I can. I keep getting asked by my peers on my opinions on NetScaler vs. F5 for Citrix delivery and I’m tired of saying the same things over and over again so that’s why I decided to write this article. Something I can just link them to from now on. 

DISCLAIMER #1
I’m biased toward NetScaler. How biased you ask? My relationship with NetScaler goes back years and years (the red and black days). Now think back to Christmas time when you were a kid growing up. Did you ever shake your wrapped presents under your Christmas tree trying to see what they were? Did you recognize the shape of a box and already have an idea of what the gift was? It’s that Hot Wheels race track set you’ve been hinting to your parents about for months, right? Remember that excitement? You couldn’t wait to tear through that gift wrap and play with it come Christmas morning. This is exactly how I feel when I get emailed a tracking number and know my MPX appliances are being delivered at the datacenter that morning. I can spot the box an MPX appliance gets shipped in from 50 ft away. To the point where I can lift up the box and tell you approximately what series appliance is in there just from the weight. Opening it up and smelling the device and the out-gassing of the cardboard and packing foam is the same as the smell of gingerbread and eggnog for me. Getting an HA pair racked, configured, and blinking Primary and Secondary are my Christmas lights. Seeing my traffic go through them and watching my policy hit counters rise is like setting up that Hot Wheels race track and watching those little cars spin around and around all Christmas day. That’s how much I love deploying NetScalers. It’s like being a kid again for me. NetScalers are magical devices and I know how to make them do whatever I dream up. Now that you REALLY know how I feel…

DISCLAIMER #2
I’m not a network engineer. Sure I can configure NetScaler, F5, Cisco, Juniper, SonicWall, etc. appliances like nobodies business from my experiences earlier in my career but I don’t consider myself a network engineer. I’m going to have more of a virtualization and application\VDI delivery spin to my opinions because that’s what I do on a daily basis. I’m not a dedicated network engineer where that is my one and only function everyday by any means. So if you want a qualified purely network engineer perspective, you’ll have to find someone else to talk to. If you want the opinion of a Citrix Architect whose life revolves around XenApp and XenDesktop delivery, keep reading.

MY OPINION ON APPLICATION DELIVERY CONTROLLERS
F5 has been around forever but I never actually got to deploy them like I have over the years with NetScaler until last year when I played with LTM APM to see how well it handles Citrix XenApp and XenDesktop delivery. NetScaler and F5 are pretty much neck to neck for basic web traffic. All the Gartner, InfoWorld, etc. reports all show around X% of the market share belonging to one, and around X% to the other depending on whatever sources they’re using. Screw the marketing statistics. Get the answers yourself. If you have peers at Fortune 500s, and ask them what they’re using for regular web traffic. Then ask them what they are using for Citrix delivery or any Cloud based initiatives and why. You’ll find that depending on the use case, the ADC they are running will usually swing one way or the other almost every time and for good reason.