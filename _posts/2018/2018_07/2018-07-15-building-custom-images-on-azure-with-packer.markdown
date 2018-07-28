---
layout: post 
title:  "Building Custom Images on Azure with Packer" 
date:   2018-07-15T10:21:11.578Z 
categories: terraform azure deployment
link: http://www.tomsitpro.com/articles/build-custom-soe-on-azure-with-packer,1-3649.html 
tags:
  - links
ogtype: article 
---

> Building Custom Images on Azure with Packer
By David O'BrienAUGUST 31, 2017 3:00 AM - Source: Toms IT Pro
     
TAGS : WindowsWindows Azure
Packer is open source, free, cross-platform written in Golang and works on all major cloud platforms.


Despite what a lot of people say, Infrastructure as a Service (IaaS) is quite difficult. One of the tasks people need to work on is creating a base image for their workloads. Just like on-premises where you would create your base SOE ("Standard Operating Environment" or "golden image"), you do the same thing in the cloud.

The process is quite simple.
     1. Take marketplace image
     n. (custom steps)
     n+1. Create custom image from marketplace image