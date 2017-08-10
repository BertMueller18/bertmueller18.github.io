---
layout: post
published: true
title: "NetScaler Website Redirection - The Nice &amp; Elegant Way"
date: 2016-09-01T22:10:22.278Z
categories: netscaler citrix
link: http://www.lewan.com/blog/netscaler-website-redirection-the-nice-elegant-way
tags:
  - links
ogtype: article
bodyclass: post
---

## NETSCALER WEBSITE REDIRECTION - THE NICE & ELEGANT WAY

 Back to all posts
 Posted by Johnny Ma  August 10, 2016

Did you know that you can configure NetScaler so users don’t have to type in the https:// when going to StoreFront or the NetScaler Gateway URLs?

More often than not, this is accomplished using a crude method in which port 80 http Virtual Server is configured on the same IP as the https site and the Redirect URL field in the protection section of the Virtual Server is set. While this works just fine, it unfortunately also renders a permanently Down Virtual Server in the Load Balancing screen.



Good news though, there is a better way to configure the redirection that renders all of the Virtual Servers as Up by using Responder Policies.
If you own a NetScaler VPX10 and above (MPX and SDX included), regardless of which edition, you have a license for Responder Policies.
