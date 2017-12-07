---
layout: post 
title:  "PowerShell DSC at a Glance – Frequently asked Questions (FAQ) – Crawl, Walk, Run, Automate" 
date:   2017-12-07T07:57:34.659Z 
categories: powershell psdsc automation
link: http://nikcharlebois.com/powershell-dsc-at-a-glance-frequently-asked-questions-faq/ 
tags:
  - links
ogtype: article 
---

> PowerShell DSC at a Glance – Frequently asked Questions (FAQ)
 2016-10-05  Nik Charlebois	 Tutorial  80 2 Comments
PowerShell Desired State Configuration (DSC) is a great way to automate the deployment of any type of environments. The DSC engine has matured a lot over the past 2 years, and is now ready for prime time within the enterprises. However, I feel like this is still a component of PowerShell that is too little known in the industry. Be it because people have not yet heard of it (it was only introduced in WMF4 after all), or because people get scare by its apparent complexity, PowerShell DSC does not yet have the exposure it should. This article aims at answering the most frequent questions I get about PowerShell DSC when I try to introduce its concepts to some of my clients. The answer to the questions are mine, and I am trying to vulgarize the concepts as much as possible.

What is PowerShell DSC?

PowerShell Desired State Configuration (DSC) is an engine within PowerShell version 4 and greater that allows a user to specify an end result configuration (a Desired State) for a machine to be in, and have it automatically configure itself to match that end result configuration.

How does it work?

The Windows Management Framework (WMF) 4 and greater include a service component called the Local Configuration Manager (LCM) that is responsible to orchestrate the configuration of the machine into its Desired State. Via PowerShell, users will create what I refer to as a DSC Configuration Script (which you shouldthink of as a definition/description of what the Desired State should be), and pass it onto the LCM for it to start automating thr configuration.