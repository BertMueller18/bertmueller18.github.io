---
layout: post 
title:  "Create mandatory user profiles (Windows 10) | Microsoft Docs" 
date:   2018-07-08T15:54:10.095Z 
categories: activedirectory deployment
link: https://docs.microsoft.com/en-us/windows/client-management/mandatory-user-profile 
tags:
  - links
ogtype: article 
---

## Create mandatory user profiles
10/16/2017

Applies to

Windows 10
A mandatory user profile is a roaming user profile that has been pre-configured by an administrator to specify settings for users. Settings commonly defined in a mandatory profile include (but are not limited to): icons that appear on the desktop, desktop backgrounds, user preferences in Control Panel, printer selections, and more. Configuration changes made during a user's session that are normally saved to a roaming user profile are not saved when a mandatory user profile is assigned.

Mandatory user profiles are useful when standardization is important, such as on a kiosk device or in educational settings. Only system administrators can make changes to mandatory user profiles.

When the server that stores the mandatory profile is unavailable, such as when the user is not connected to the corporate network, users with mandatory profiles can sign in with the locally cached copy of the mandatory profile, if one exists. Otherwise, the user will be signed in with a temporary profile.

User profiles become mandatory profiles when the administrator renames the NTuser.dat file (the registry hive) of each user's profile in the file system of the profile server from NTuser.dat to NTuser.man. The .man extension causes the user profile to be a read-only profile.