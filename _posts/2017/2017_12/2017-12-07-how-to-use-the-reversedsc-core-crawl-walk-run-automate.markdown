---
layout: post 
title:  "How to use the ReverseDSC Core – Crawl, Walk, Run, Automate" 
date:   2017-12-07T07:56:12.230Z 
categories: powershell psdsc automation
link: http://nikcharlebois.com/how-to-use-the-reversedsc-core/ 
tags:
  - links
ogtype: article 
---

## How to use the ReverseDSC Core
 2017-01-13  Nik Charlebois	 Tutorial  248 Leave a comment
The ReverseDSC.Core module is the heart of the ReverseDSC process. This module defines several functions that will help you dynamically extract the DSC configuration script for each resource within a DSC module. The ReverseDSC Core is generic, meaning that it applies to any technology, not only SharePoint. In this blog article I will describe in details how you can start using the ReverseDSC Core module today and integrate it into your existing solutions. To better illustrate the process, I will be using an example where I will be extracting the properties of a given user within Active Directory using the ReverseDSC Core.