---
layout: post 
title:  "PowerShell Advanced Function Template - It For Dummies" 
date:   2017-04-24T11:45:41.855Z 
categories: powershell programming
link: https://itfordummies.net/2017/04/24/powershell-advanced-function-template/ 
tags:
  - links
ogtype: article 
---

> PowerShell Advanced Function Template
Posted on April 24, 2017 by edemilliere
PowerShell Advanced Function Template

Hello,

Today, we’ll see how to write a basic advanced function by using a wide variety of PowerShell features. We’ll try to use all the features provided by Microsoft to write a advanced function with the minimum of lines possible.

First, let list the features we want in our advanced function:

Error handling
Verbose
Parameter Validation
Pipeline utilization
To achieve this, we need to use:

Try/Catch
CmdletBinding
ValidatePattern/ValidateScript/Validate*
Parameter()
Hereunder a dummy example that use all of them:

First, a test function, to check behavior: