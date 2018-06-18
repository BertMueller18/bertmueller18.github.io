---
layout: post 
title:  "Citrix Profile Management Part-1" 
date:   2018-06-08T19:31:21.599Z 
categories: citrix upm xenapp xendesktop
link: http://www.virtualvemula.com/2018/05/citrix-profile-management-part-1.html?spref=tw 
tags:
  - links
ogtype: article 
---

## Citrix Profile Management Part-1
May 24, 2018
Before we discuss about Citrix Profile Manager, let us try to understand what a profile is, what are the different type of profiles that we have and Benefits of each type of profile Citrix user profile is nothing but a Windows user profile. Citrix uses Windows user profiles when users access Published Desktop or Application through Citrix.

Windows User Profile is folder that gets created with user loginid under C:\Users directory when user logs on to a Windows Machine. The content of User profile folder includes Desktop, My Documents, Favourites, Downloads, AppData etc. It will also store configuration settings, Registry Settings, Printer Settings, and Network Settings etc of the user. User registry configuration is stored separately for each user in a file called NTUSER.dat which gets imported to HKCU or HKEY_CURRENT_USER registry hive.

When user log onto a Machine for the first time, a profile using his/her user id will get created with a copy of Default user profile. Default user profile gets created under C:\Users during the OS install along with Public Profile.

While Default profile is used to create user profiles, Public profile is used to share files or folders to all the users, which means if a file is copied to Desktop folder of Public Profile it is visible for all the users on their Desktop.
