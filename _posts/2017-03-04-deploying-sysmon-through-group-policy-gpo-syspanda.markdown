---
layout: post 
title:  "Deploying Sysmon through Group Policy (GPO) – Syspanda" 
date:   2017-03-04T20:34:35.836Z 
categories: sysmon eventlog gpo
link: http://syspanda.com/index.php/2017/02/28/deploying-sysmon-through-gpo/ 
tags:
  - links
ogtype: article 
---

## Deploying Sysmon through Group Policy (GPO)
by Pablo Delgado on February 28, 2017 in Sysmon
Here’s a way to deploy Sysmon to all of your domain endpoints using Group Policy.

Step1: Create sysmon install batch file

First create a batch file that will be placed on the root domain folder that is accessible to each domain client.

Here’s the batch file: