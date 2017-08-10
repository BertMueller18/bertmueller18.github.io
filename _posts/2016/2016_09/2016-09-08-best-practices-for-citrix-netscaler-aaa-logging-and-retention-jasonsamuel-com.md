---
layout: post
published: true
title: "Best practices for Citrix Netscaler AAA logging and retention – JasonSamuel.com"
date: 2016-09-08T08:28:13.423Z
categories: citrix netscaler monitoring
link: http://www.jasonsamuel.com/2014/05/28/best-practices-for-citrix-netscaler-aaa-logging-and-retention/
tags:
  - links
ogtype: article
bodyclass: post
---

> CITRIX NETSCALERBest practices for Citrix Netscaler AAA logging and retentionBy Jason Samuel
onMay 28, 2014
1SHARESHARE TWEET SHARE SHARE 3 COMMENTS


By default the Netscaler is set to certain log levels for certain modules on the device, including AAA (authentication, authorization and accounting) logging. Sometimes you may want to change the AAA log retention temporarily for easier troubleshooting.

I’ve posted several articles around Netscaler AAA already but if you’re new to it, AAA logging is saved to the /var/log/ns.log file (and all subsequent rollover files i.e ns.log.0.gz, ns.log.1.gz, ns.log.2.gz, etc.) and you can view these via GUI by going to System > Auditing > then clicking on “Syslog messages”. Once the window loads, in the Module drop down choose “AAA” or whatever you are trying to filter for and hit “Find Now”. Choose the logs in the bottom left (just doubleclick).



The default setting for AAA logs is set to save the last 25 log files (circular logging where it will overwrite the oldest) and the size is set to 100 Kilobytes. Not a whole lot. The best practice is not to utilize the device itself for historical logs. It’s really only meant to be used for realtime/neartime logs for troubleshooting purposes. Historical Netscaler AAA logs should be offloaded from the appliance using a syslog server. It’s very easy to configure. Just go to Auditing > Syslog and add your syslog server and policy. Make sure you select “ALL” events. It’s always best to have more and let your syslog server do it’s thing than try and filter on the device and end up with something you needed missing. Forward it all. Your syslog server should be sized to take it and retain the data for whatever period your information security/compliance policy dictates.

If you don’t have a syslog server availab
