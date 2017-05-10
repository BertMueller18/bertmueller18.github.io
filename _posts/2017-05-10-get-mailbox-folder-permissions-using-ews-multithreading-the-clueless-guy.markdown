---
layout: post 
title:  "Get mailbox folder permissions using EWS multithreading | The clueless guy" 
date:   2017-05-10T15:38:43.032Z 
categories: exchange ews powershell
link: https://ingogegenwarth.wordpress.com/2015/04/16/get-mailbox-folder-permissions-using-ews-multithreading/ 
tags:
  - links
ogtype: article 
---

> Get mailbox folder permissions using EWS multithreading
Posted on April 16, 2015
A few weeks ago I was involved in a migration project. At one point in time we needed a script to retrieve permissions on mailboxes on folder-level. Besides this we needed to read the property PR_NT_SECURITY_DESCRIPTOR for folders.

Why we needed to read the property PR_NT_SECURITY_DESCRIPTOR?

Read more about in this article here!

Now back to the script. I know there are many scripts out there, which are doing this job. But we needed something to get the data real quick and a way to retrieve SIDs. I started looking for all options and ended in .NET mutlithreading for the first and MrMAPI for the second need.