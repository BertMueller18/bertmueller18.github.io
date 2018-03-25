---
layout: post 
title:  "MDT/OSD Driver Management overview | Keith's Consulting Blog" 
date:   2018-03-25T15:11:38.028Z 
categories: mdt drivermanagement deployment
link: https://keithga.wordpress.com/2013/12/09/mdtosd-driver-management-overview/ 
tags:
  - links
ogtype: article 
---

> MDT/OSD Driver Management overview
Wanted to write down some notes on various Device Driver deployment issues related to MDT and SCCM.

I had done some work recently with Microsoft IT with their latest Windows 8 roll out using MDT 2012. It was quite enlightening to see some real world device driver installation issues get worked out. The Microsoft IT OS Deployment team had an extensive lab where they had at least one of every kind of officially supported machine present for us to do some testing on.

First thing I did was add my previously released ZTIYellowBang.wsf script to our standard Task Sequence. Then I would get a report of every device that was missing a driver at the end of the deployment. This helped speed things up during the early phases. I didn’t have to go to each machine and get the PnP ID for the missing device, the information was automatically copied to the logging server share, all I had to do was grep the output looking for errors.