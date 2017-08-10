---
layout: post
published: true
title: "How to load balance Citrix Director 7.6 using a Citrix NetScaler – JasonSamuel.com"
date: 2016-09-08T08:26:26.593Z
categories: loadbalancer netscaler citrix xenapp xendesktop 
link: http://www.jasonsamuel.com/2015/06/02/how-to-load-balance-citrix-director-7-6-using-a-citrix-netscaler/
tags:
  - links
ogtype: article
bodyclass: post
---

## How to load balance Citrix Director 7.6 using a Citrix NetScalerBy Jason Samuel
onJune 2, 2015
2SHARESSHARE TWEET SHARE SHARE 4 COMMENTS


Citrix Director is a very important piece of any XenDesktop or XenApp environment. You don’t want to have a single point of failure for this, especially if your help desk relies on it. I saw a Twitter post the other day asking how to load balance Director 7.6 and figured I’d write up this guide. I also have a couple of BONUS tricks that will make Director easier to use for your end users.

Citrix Director should not be used on your Delivery Controllers in large production environments. It’s a pretty heavy web app and the more users you have using it the more load there will be on your Delivery Controllers. The best thing to do is setup separate dedicated web servers for the Director role. Also note it’s best practice to have a separate SQL databases for Site configuration, Logging, and Monitoring but most all 7.6 deployments I’ve seen in the real world have it all combined (and I blame the Citrix installation wizard for this, they should made it easier for folks to understand and change during installation). In this example I’m going to assume you have setup 2 dedicated Director 7.6 servers and connected them to your Delivery Controllers. On the NetScaler, the config is no different than any other website you would load balance:
