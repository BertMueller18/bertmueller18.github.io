---
layout: post
published: true
title: "Combating Citrix application sprawl using the XenApp SDK, Powershell, IIS, HTML, and a tiny bit of web design – JasonSamuel.com"
date: 2016-09-08T08:29:50.727Z
categories: citrix xenapp xendesktop monitoring
link: http://www.jasonsamuel.com/2013/10/07/combating-citrix-application-sprawl-using-the-xenapp-sdk-powershell-iis-html-and-a-tiny-bit-of-web-design/
tags:
  - links
ogtype: article
bodyclass: post
---

## Combating Citrix application sprawl using the XenApp SDK, Powershell, IIS, HTML, and a tiny bit of web designBy Jason Samuel
onOctober 7, 2013
1SHARESHARE TWEET SHARE SHARE 8 COMMENTS
One of the biggest challenges you will face in a large XenApp environment is application sprawl. With multiple farms and many Citrix admins managing different business units, the problem gets compounded. No one person knows what applications are published and to what security groups without having to hunt for it.

I’ve used a lot of 3rd party applications for monitoring and reporting on XenApp but none of them quite showed the information I wanted in an easily digestible format. So I created a solution using the XenApp SDK, Powershell, and IIS. I wanted to create nicely formatted HTML reports with all the application details and have them available via a website URL so anyone can take a look at it whenever they needed to. My audience could be a Citrix admin, an IT manager, a security department, or even a compliance auditor. I wanted the info at our fingertips and be fully automated and up to date. Think of it as a dashboard view into your Citrix environment.

So let me show you how I did it.
