---
layout: post 
published: true 
title: "Create a custom Deployment Wizard pane for Updates (MDT) | MicaH's IT blog" 
date: 2016-10-06T08:00:22.186Z
categories: mdt deployment 
link: https://itmicah.wordpress.com/2014/01/25/create-a-custom-deployment-wizard-pane-for-updates-mdt/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Create a custom Deployment Wizard pane for Updates (MDT)
Posted on January 25, 2014 by MicaH
Note: This blogpost is also posted on the peppercrew website.

The Story

One of the great things about the Microsoft Deployment Toolkit (MDT) is that it’s a very open product. All the scripts are customizable, including the Deployment Wizard. We can add new functionality to the deployment procedure and add wizard pages so we can choose to use those new functions (or not) with each new deployment. Microsoft encourages creativity for this particular product. One of the functions I wanted to create a wizard page for was the deployment of updates. I wanted to be able to choose between a quick OS deployment for test purposes (no updates) and a slower, more production worthy deployment (with updates). And since I take my deployment VM on the road with me, I wanted the ability to choose if the updates are downloaded from Microsoft Update or a clients’ WSUS server.