---
layout: post 
published: true 
title: "Apple OS X Security Configuration Audit: osxlockdown" 
date: 2016-07-22T18:11:32.072Z 
link: https://n0where.net/apple-os-x-security-configuration-audit-osxlockdown/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Apple OS X Security Configuration Audit

osxlockdown was built to audit, and remediate, security configuration settings on OS X 10.11 (El Capitan).

This checks, and if requested will flip, various configuration settings. Many are simply stripping out features to reduce the attack surface. You may not like this. This is a compilation of numerous resources listed in the Resources section which could be converted to bash scripts. This is different than those resources in that instead of requiring the user to read a 100+ page doc, click through numerous GUIs, and try to decide if some esoteric output is good or bad, this tool combines all the steps into a single command. This tool is focused on enterprise deployments of OSX with regard to what it does, but made to be usable for stand-alone home users as well.

Warning: Many of the rules disable functionality in the name of security. This may make you sad.

Warning: System commands and dark arts are involved, so ensure you have your system backed up first. No problems have been reported so far though.