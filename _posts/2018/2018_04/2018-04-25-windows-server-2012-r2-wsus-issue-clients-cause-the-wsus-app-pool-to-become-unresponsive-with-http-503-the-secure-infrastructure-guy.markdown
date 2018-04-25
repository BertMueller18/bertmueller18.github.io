---
layout: post 
title:  "Windows Server 2012 R2 WSUS Issue: Clients cause the WSUS App Pool to become unresponsive with HTTP 503 – The Secure Infrastructure Guy" 
date:   2018-04-25T20:49:12.223Z 
categories: wsus maintenance
link: https://blogs.msdn.microsoft.com/the_secure_infrastructure_guy/2015/09/02/windows-server-2012-r2-wsus-issue-clients-cause-the-wsus-app-pool-to-become-unresponsive-with-http-503/ 
tags:
  - links
ogtype: article 
---

## Windows Server 2012 R2 WSUS Issue: Clients cause the WSUS App Pool to become unresponsive with HTTP 503
★★★★★★★★★★★★★★★
Christian PresleySeptember 2, 201513 
0
0
Something interesting that I recently uncovered while implementing WSUS with Windows Server 2012 R2 as Software Update Points in Configuration Manager. The WSUS App Pool by default has relatively low Rapid-Fail Protection thresholds. These thresholds were causing the WSUS Web Service to eventually lock-out with HTTP 503.

The errors are associated with these events:

Log Name: Application
Source: Windows Server Update Services
Event ID: 12072
The WSUS content directory is not accessible.
System.Net.WebException: The remote server returned an error: (503) Server Unavailable.
   at System.Net.HttpWebRequest.GetResponse()
   at Microsoft.UpdateServices.Internal.HealthMonitoring.HmtWebServices.CheckContentDirWebAccess(EventLoggingType type, HealthEventLogger logger)
 
Log Name: Application
Source: SMS Server
Event ID: 7000
On 8/13/2015 3:22:40 AM, component SMS_WSUS_CONTROL_MANAGER on computer WSUS.fqdn reported:  WSUS Control Manager failed to configure proxy settings on WSUS Server "WSUS.fqdn".
Possible cause: WSUS Server version 3.0 SP2 or above is not installed or cannot be contacted.
Solution: Verify that the WSUS Server version 3.0 SP2 or greater is installed. Verify that the IIS ports configured in the site are same as those configured on the WSUS IIS website.You can receive failure because proxy is set but proxy name is not specified or proxy server port is invalid.
 
Log Name: System
Source: Microsoft-Windows-WAS
Event ID: 5074
A worker process with process id of '%1' serving application pool '%2' has requested a recycle because the worker process reached its allowed processing time limit.
