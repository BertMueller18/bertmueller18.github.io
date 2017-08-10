---
layout: post
published: true
title: "How to use Citrix Netscaler Insight Center to report on web, HDX, and Access Gateway (AGEE) traffic – JasonSamuel.com"
date: 2016-09-08T08:30:18.231Z
categories: netscaler monitoring citrix networking
link: http://www.jasonsamuel.com/2013/06/17/how-to-use-citrix-netscaler-insight-center-to-report-on-web-hdx-and-access-gateway-agee-traffic/
tags:
  - links
ogtype: article
bodyclass: post
---

## CITRIX INSIGHT CENTER How to use Citrix Netscaler Insight Center to report on web, HDX, and Access Gateway (AGEE) trafficBy Jason Samuel
onJune 17, 2013
2SHARESSHARE TWEET SHARE SHARE 11 COMMENTS
I love Netscalers, they’re my favorite Citrix product. But one of the features I have always felt they are a bit lacking on was reporting. You might get requests from management asking how many users are hitting the Access Gateway (AGEE), when are they logging in, what is the session duration, etc. There is some pretty good data in the Netscaler dashboard but it is real time. Not historical. In the past, I have personally used the following for historical reporting on AGEE and any of my load balanced vservers:

1. 3rd party tool like Solarwinds utilizing via SNMP on the Netscaler
2. Enabling web logging on the Netscaler and extracting the data I need using LogParser
3. Using Citrix EdgeSight to report on clients (WI/StoreFront vs. PNAagent traffic) but hard to segment multiple traffic sources (especially when a XenDesktop session is launched and apps are launched through Citrix Receiver Enterprise/PNAgent via Start menu which will always appear as local traffic)
4. Using Netscaler Reporting Tool
