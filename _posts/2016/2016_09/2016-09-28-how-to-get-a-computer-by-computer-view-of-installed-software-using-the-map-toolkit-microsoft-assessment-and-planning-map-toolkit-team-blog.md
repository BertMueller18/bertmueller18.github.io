---
layout: post 
published: true 
title: "How to get a computer by computer view of installed software using the MAP toolkit – Microsoft Assessment and Planning (MAP) Toolkit Team Blog" 
date: 2016-09-28T14:09:46.563Z
categories: activedirectory inventory map
link: https://blogs.technet.microsoft.com/mapblog/2013/01/28/how-to-get-a-computer-by-computer-view-of-installed-software-using-the-map-toolkit/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> How to get a computer by computer view of installed software using the MAP toolkit
★★★★★★★★★★★★★★★
Rob Polly - MicrosoftJanuary 28, 20132
0
0
0
One of the most frequent questions we get at MAPFDBK@microsoft.com is how to get a list of the software discovered by the MAP toolkit on a computer by computer basis.  Most of the users who ask are using this to help them answer a licensing question but it can be used in a number of other scenarios as well for example Software Asset Management or user profiling for VDI (see http://blogs.technet.com/b/mapblog/archive/2012/07/09/planning-for-desktop-virtualization-with-the-map-toolkit-7-0-4-of-4.aspx). 

In MAP 7.0, provided this information through a database view and Microsoft Excel.  The name of the view is InstalledProducts_view.

In MAP 8.0, this view has been renamed to [UT_WinServer_Reporting].[InstalledProductsView].