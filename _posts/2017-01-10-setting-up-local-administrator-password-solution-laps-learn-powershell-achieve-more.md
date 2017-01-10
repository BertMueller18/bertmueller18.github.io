---
layout: post 
title:  "Setting up Local Administrator Password Solution (LAPS) | Learn Powershell | Achieve More" 
date:   2017-01-10T15:35:58.629Z 
categories: activedirectory laps powershell
link: https://learn-powershell.net/2016/10/08/setting-up-local-administrator-password-solution-laps/ 
tags:
  - links
ogtype: article 
---

> Setting up Local Administrator Password Solution (LAPS)
Posted on October 8, 2016 by Boe Prox
I decided to spend some time implementing LAPS in my lab as it is Microsoft’s solution to local administrator account password management. Why would I want something like this in my environment? Great question! Most organizations probably use the same password (maybe a slightly modified password based on each client…maybe) that ensures that the people who help manage the workstations have a way to log into the system should the computer lose its network configuration or some other issue where the only way to troubleshoot might he to log into the workstation using the local administrator account.

This is great until you someone such as an insider threat manages to get control of the password to the administrator account and now has a way to laterally move around the network from host to host until they can elevate their account to a domain admin. And at that point we know it is game over.