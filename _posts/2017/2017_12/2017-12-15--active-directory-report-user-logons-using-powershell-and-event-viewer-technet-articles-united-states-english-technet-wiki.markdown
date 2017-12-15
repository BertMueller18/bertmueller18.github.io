---
layout: post 
title:  "	Active Directory: Report User logons using PowerShell and Event Viewer - TechNet Articles - United States (English) - TechNet Wiki" 
date:   2017-12-15T19:44:50.588Z 
categories: activedirectory reporting powershell
link: https://social.technet.microsoft.com/wiki/contents/articles/37531.active-directory-report-user-logons-using-powershell-and-event-viewer.aspx 
tags:
  - links
ogtype: article 
---

> Active Directory: Report User logons using PowerShell and Event Viewer
Table of Contents
Introduction
Preparation
Running the script
How it works?
Understanding the process
Explaining the script
Param section
Begin section
Process section
End Section
Conclusion
See Also
Introduction
As you know, the concept of auditing in an Active Directory environment, is a key fact of security and it is always wanted to find out what a user has done and where he did it. One of the important task that most of the administrators are dealing these days is to find out where a user has logged on.

Today we will walk through a step-by-step guide in which you will learn how to utilize built-in Event Viewer on domain controllers for your favorite report and specifically, find where a user has logged on.

To make things more understandable, take a look at the attached  image below in which you can find what do we mean by list of computers where a user account has logged on since past days. This picture consider (m.tehrani) user account as an example: