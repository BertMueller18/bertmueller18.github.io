---
layout: post 
published: true 
title: "User Profile and Home Directory Storage: Distributing the Load Across Multiple File Servers • Helge Klein" 
date: 2016-09-27T06:22:18.914Z 
categories: citrix windows activedirectory
tags: citrix windows activedirectory 
link: https://helgeklein.com/blog/2009/04/user-profile-and-home-directory-storage-distributing-the-load-across-multiple-file-servers/ 
  - links
ogtype: article 
bodyclass: post 
---

> User Profile and Home Directory Storage: Distributing the Load Across Multiple File Servers

by Helge Klein on April 13, 2009 in User Profiles
This article is part of Helge’s Profile Toolkit, a set of posts explaining the knowledge and tools required to tame Windows user profiles.

The easiest way to assign user profile and home directories is via group policy. But that can only be done per computer. There is no (simple) way to point different users’ directories to different file servers. So what? No problem at all, until the number of users is too large for a single file server to handle. This article discusses what can be done to spread the user load.