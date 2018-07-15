---
layout: post 
title:  "Best Practices with Packer and Windows" 
date:   2018-07-15T10:20:44.410Z 
categories: terraform hyperv deployment
link: https://hodgkins.io/best-practices-with-packer-and-windows 
tags:
  - links
ogtype: article 
---

> Best Practices with Packer and Windows
Why you should be using Packer
Getting Started with Packer
Best Practices
Step by Step
Generic Templates
Use guest additions mode of attach
Use environment variables to change the action of a provisioning script
Keep the OS information in your build script
Disable WinRM on build completion and only enable it on first boot
Use headless mode
Set a high shutdown and WinRM timeouts
Conclusion
Why you should be using Packer
Already know why Packer is useful? Jump directly to the best practices.

When you develop automation, for example, PowerShell Desired State configuration resources, where do you test them?

If the answer is locally on your machine or a remote Virtual Machine platform, you are missing out on some opportunities of speed and reduction in your development and test cycle time.

Have a look at Gael Colas’s awesome introduction to Test-Kitchen and Kitchen-DSC, which will show you how to develop and test your DSC resources easily on your local machine inside Virtual Machines.

