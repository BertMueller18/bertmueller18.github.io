---
layout: post 
published: true 
title: "Support Tip: Mandatory user profiles and App-V integration with Configuration Manager – The Official Microsoft App-V Team Blog" 
date: 2016-10-06T07:10:21.327Z 
link: https://blogs.technet.microsoft.com/appv/2016/05/16/support-tip-mandatory-user-profiles-and-app-v-integration-with-configuration-manager/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Support Tip: Mandatory user profiles and App-V integration with Configuration Manager
★★★★★★★★★★★★★★★
J.C. Hornbeck [MSFT]May 16, 20162
0
2
0
Hi everyone, Luke Ramsdale here with a tip for you on using mandatory user profiles in an integrated App-V/ConfigMgr environment.

There are a number of scenarios where an organization may require that the user profiles on their workstations not be stored locally. For example, maybe mandatory profiles are configured or the profiles are deleted after the user logs off, or VDI machines are in use and are not persistent. When an organization uses Microsoft Application Virtualization (App-V) integrated with Configuration Manager, this scenario can lead to problems when deploying virtual applications to collections of users. This is because when the user profile is returned to its mandatory state, or it is deleted after logging off, the App-V files stored in the user profile are also deleted. This proves problematic when the users eventually log back on to the machines because the shortcuts and part of the virtual applications are not available until the application deployment evaluation cycle runs, which is by default every 7 days.