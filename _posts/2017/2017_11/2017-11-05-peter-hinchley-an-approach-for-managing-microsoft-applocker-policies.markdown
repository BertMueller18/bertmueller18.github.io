---
layout: post 
title:  "Peter Hinchley : An Approach for Managing Microsoft AppLocker Policies" 
date:   2017-11-05T07:11:36.683Z 
categories: applocker
link: https://hinchley.net/articles/an-approach-for-managing-microsoft-applocker-policies/ 
tags:
  - links
ogtype: article 
---

## An Approach for Managing Microsoft AppLocker Policies

AppLocker is a software whitelisting product from Microsoft that ships with Windows. It can be used to restrict the software that will execute on a computer.

Overview of Policies
AppLocker policies are typically created and deployed using Group Policy. If multiple policies are deployed to a single computer, these policies are merged into a single "effective" policy (more on this later).

