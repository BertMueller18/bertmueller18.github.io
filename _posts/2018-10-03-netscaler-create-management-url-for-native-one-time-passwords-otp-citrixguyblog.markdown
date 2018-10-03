---
layout: post 
title:  "NetScaler – Create Management URL for Native One Time Passwords (OTP) – CitrixGuyBlog" 
date:   2018-10-03T21:35:39.867Z 
categories: netscaler citrix totp otp 2fa mfa
link: https://citrixguyblog.com/2017/10/18/netscaler-create-management-url-for-native-one-time-passwords-otp/ 
tags:
  - links
ogtype: article 
---

## NetScaler – Create Management URL for Native One Time Passwords (OTP)

The OTP feature which is available since NetScaler 12.0 Build 51.24 is a great feature to reduce your operationg costs or implement 2 factor authentication for the first time because your company/customer wanted to save some money instead of investing in  secure remote access 

If you already have configured the AAA server, schemas and the authenciation policies you should be able to access the OTP Management Web GUI with the substring “/manageotp” on your NetScaler Gateway. If this is not the case please follow Carl Stalhoods  detailed configuration steps.