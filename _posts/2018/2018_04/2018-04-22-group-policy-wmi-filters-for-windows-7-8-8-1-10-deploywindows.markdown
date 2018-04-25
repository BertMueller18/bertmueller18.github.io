---
layout: post 
title:  "Group Policy WMI filters for Windows 7/8/8.1/10 – DeployWindows" 
date:   2018-04-22T21:26:39.579Z 
categories: activedirectory gpo wmi
link: https://deploywindows.com/2016/11/03/group-policy-wmi-filters-for-windows-788-110/ 
tags:
  - links
ogtype: article 
---

 Group Policy WMI filters for Windows 7/8/8.1/10

Date: November 3, 2016
Author: Mattias Fors
8 Comments
Every now and then during Windows 10 deployments we need to use WMI filters for group policy objects, there are simply no better way of doing this, without a lot of work. WMI is simple to use and demands little maintenance.

There WMI filters may also come handy since there are group policy settings that only applies to one or two builds.

So here are some examples, ready to use for all operating system.

There are three queries for all operating system, 64-bit, 32-bit and both.

Note! Due to performance do NOT use Select * instead use Select Version as in the queries below, Why? See this article Using group policy WMI filters computers booting slow?