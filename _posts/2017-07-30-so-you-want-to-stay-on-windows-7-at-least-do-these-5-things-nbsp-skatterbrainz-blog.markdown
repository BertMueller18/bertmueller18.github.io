---
layout: post 
title:  "So, you want to stay on Windows 7. At least do these 5 things…&nbsp; – Skatterbrainz Blog" 
date:   2017-07-29T22:32:51.662Z 
categories: win7 smb1 security activedirectory
link: https://skatterbrainz.wordpress.com/2017/07/01/so-you-want-to-stay-on-windows-7-at-least-do-these-5-things/ 
tags:
  - links
ogtype: article 
---

> So, you want to stay on Windows 7. At least do these 5 things… 

      Rate This



I have a few customers, that for a variety of reasons, are staying on Windows 7 for a while longer. I don’t necessarily agree with most of them, but I don’t have the magic Darth Vader power ring that forces them to reconsider.

Thankfully, that number is very small. But based on the laws of statistical sampling, I have to assume there are a significant number of others out there hiding under a rock. For the record, I’ve yet to hear a reason that holds water. Most are based on emotion or FUD, or fear of vendor confrontation. 

The budget argument doesn’t hold water either, unless you’re a non-profit that lost all its donors. A for-profit business should be able to rationalize the delayed cost aspects and realize it doesn’t get cheaper from an aggregate metric. And if that isn’t enough, you have ask yourself why you’re still in business. That’s another discussion for beer, pizza and a batting cage. 

Regardless, if you just aren’t going to make the move to Windows 10 anytime soon, here’s a few things I STRONGLY recommend putting into place as soon as possible. Immediately if possible… 

Remove local administrative rights for all users. That’s right, all users. Especially executives. Why include the feared golfer group? Because they are target zero for a hungry hacker. After them would be IT admins and IT minions. IT admins should be using separate privileged accounts. 
Keep everything patched. If you have a patching process in place already, double check that it’s really working. So many customers are convinced it’s fine, and when they actually look again, they find gaping holes. If you don’t anything in place yet, WSUS is free, and it’s better than nothing. 
Remove SMBv1. I don’t need to elaborate on this. If you’re not aware of this, search “smb v1 why remove” And it doesn’t matter if you’re 7, 8, 8.1 or 10, remove it. 
Leave UAC and Windows Firewall turned on. I can count the valid reasons for disabling UAC on one finger. And it’s probably not the reason you think it is.
Start lab testing now. Build a few physical and virtual machines, load them up with all your apps and get users on them to see what works and what doesn’t. Make sure they’re configured to meet the previous 4 rules. Note any problems and start finding solutions now. 
