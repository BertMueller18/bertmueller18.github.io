---
layout: post 
title:  "Born to Automate : ELK" 
date:   2018-03-25T15:50:14.199Z 
categories: elkstack powershelldsc eventlog
link: https://blogsprajeesh.blogspot.de/search/label/ELK 
tags:
  - links
ogtype: article 
---

> Combining DSC with ELK for effective infrastructure monitoring
DSC and event logs

DSC the management platform in Windows PowerShell that enables deploying and managing configuration data for software services and managing the environment in which these services run.
DSC provides a set of Windows PowerShell language extensions, new Windows PowerShell cmdlets, and resources that you can use to declaratively specify how you want your software environment to be configured. It also provides a means to maintain and manage existing configurations. When you run a DSC configured resource on a target system it will first check if the target matches the configured resource. If it doesn’t match it, it will make it so.

But if there is an error in the last DSC run? How can we have live monitoring and alerting with DSC? We’ll that’s what we’ll be solving in this post. We’ll use the combination of event logs and the ELK stack to create an infrastructure monitoring system, for our environments. DSC logs every details of the execution and details in the windows event logs. These logs can be found by using the EventViewer, by navigating to the channel Applications and Service Logs -> Microsoft -> Windows -> Desired State Configuration. 