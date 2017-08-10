---
layout: post
published: true
title: "How to deploy Microsoft Azure MFA &amp; AD Connect with Citrix NetScaler Gateway – JasonSamuel.com"
date: 2016-09-08T08:25:59.489Z
categories: citrix netscaler mfa 2fa security
link: http://www.jasonsamuel.com/2015/09/18/how-to-deploy-microsoft-azure-mfa-ad-connect-with-citrix-netscaler-gateway/
tags:
  - links
ogtype: article
bodyclass: post
---

## How to deploy Microsoft Azure MFA & AD Connect with Citrix NetScaler GatewayBy Jason Samuel
onSeptember 18, 2015
1SHARESHARE TWEET SHARE SHARE 8 COMMENTS


I’ve deployed a lot of 2 factor authentication products with Citrix NetScaler Gateway in my career but the one I’ve always liked a lot is Microsoft Azure Multi-Factor Authentication (MFA). I used to deploy this product years ago when it was called PhoneFactor. Microsoft purchased PhoneFactor in 2012 and I was worried that would be the end of the service. But Microsoft has really taken the product to the next level.

There are several steps involved in deploying it now that PhoneFactor is integrated with Microsoft Azure. I’m going to break it down step-by-step for you and cover the following in this article:


Why You Should Deploy a 2 Factor Or Multi-Factor Authentication Solution
Setting Up Azure Active Directory
Setting Up Azure AD Connect
Setting Up Azure AD Premium
Setting Up Azure Multi-Factor Authentication Server On Premise
Configuring Azure MFA Server For NetScaler Gateway
Configuring NetScaler Gateway To Use MFA
Modifying NetScaler Gateway Logon Page For MFA
Troubleshooting MFA Authentication Issue
Auditing & Reporting MFA Logins
Azure MFA Hacking Attempt Notifications
Consider Deploying the Azure MFA User Portal For Self Service
Final Thoughts
