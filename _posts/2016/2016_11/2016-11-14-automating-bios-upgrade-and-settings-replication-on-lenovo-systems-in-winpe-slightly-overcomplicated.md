---
layout: post
published: true
title: "Automating BIOS upgrade and settings replication on Lenovo systems in WinPE | Slightly Overcomplicated"
date: 2016-11-14T13:46:46.092Z
categories: deployment 
link: https://slightlyovercomplicated.com/2015/10/14/automating-bios-upgrade-and-settings-replication-on-lenovo-systems-in-winpe/
tags:
  - links
ogtype: article
bodyclass: post
---

> Automating BIOS upgrade and settings replication on Lenovo systems in WinPE
POSTED BY MIETEK ROGALA ⋅ 2015-10-14	⋅ 3 COMMENTS
In my line of work BIOS upgrade/downgrade is a topic that keeps coming back quite frequently. Along with actual BIOS firmware update there also may be few settings that need to be applied and if you are dealing with bulk deployments – it makes sense to automate the process to save time and eliminate human error. Lenovo has a few tools out there to do the job, yet throughout the years I have found that they are not necessarily well-documented. This post gives you an outline of challenges I had to face back in the day, with an example script of automating outlined tasks on Lenovo T450 laptop.
