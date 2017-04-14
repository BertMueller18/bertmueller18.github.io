---
layout: post 
title:  "UC Unleashed » Function: Set-AdminUser – Clear AdminCount and Enable Security Inheritance" 
date:   2017-04-14T19:23:08.541Z 
categories: activedirectory security powershell
link: https://www.ucunleashed.com/1621 
tags:
  - links
ogtype: article 
---

> Function: Set-AdminUser – Clear AdminCount and Enable Security Inheritance
October 22nd, 2012Pat RichardLeave a commentGo to comments
Description
While migrating some users during a Lync migration, I needed to disable users for Lync in one forest, and enable them in another. I ran into a problem where many users in the legacy forest had adminCount set to 1, and security inheritance disabled. The problem is that my account didn’t have rights to disable them in Lync, and I was getting an access denied error. This is common when the user is/was a member of a protected group. I won’t go into the background of adminCount, as it’s well documented.

