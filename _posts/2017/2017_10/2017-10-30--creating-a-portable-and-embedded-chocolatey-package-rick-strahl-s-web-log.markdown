---
layout: post 
title:  "	Creating a portable and embedded Chocolatey Package - Rick Strahl's Web Log" 
date:   2017-10-30T16:20:12.819Z 
categories: chocolatey powershell deployment
link: https://weblog.west-wind.com/posts/2017/Jan/29/Creating-a-portable-and-embedded-Chocolatey-Package 
tags:
  - links
ogtype: article 
---

> Creating a portable and embedded Chocolatey Package
 January 29, 2017 - from Maui, Hawaii
    


Over the last few weeks I've been getting quite a few requests for a portable Chocolatey package for Markdown Monster. A zip file version of a portable install has been available for some time from the download page, but a Chocolatey package certainly would streamline the process quite a bit more.

So a couple of weeks ago I finally also put out a portable Chocolatey package and in this post I want to describe the process of creating a portable package, both from creating a low impact installation and for creating an embedded Chocolatey package that contains all the raw source files embedded in the chocolatey package.

But first lets talk Chocolatey - yumm - in general and also about creating standard packages.