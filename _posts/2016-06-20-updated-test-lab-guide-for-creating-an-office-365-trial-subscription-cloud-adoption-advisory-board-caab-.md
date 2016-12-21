---
layout: post 
published: true 
title: "Updated Test Lab Guide for creating an Office 365 Trial Subscription | Cloud Adoption Advisory Board (CAAB)" 
date: 2016-06-20T21:47:16.941Z
categories: o365
link: https://blogs.technet.microsoft.com/solutions_advisory_board/2016/06/20/updated-test-lab-guide-for-creating-an-office-365-trial-subscription/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

# Updated Test Lab Guide for creating an Office 365 Trial Subscription

The new Test Lab Guide: Create and Configure an Office 365 Trial Subscription describes how to build out the following test environment:

A simplified organization intranet connected to the Internet, hosted in Microsoft Azure infrastructure services. This intranet has the corp.contoso.com Windows Server AD domain (DC1), a general application server (APP1), and a client/admin computer (CLIENT1).  You can build this intranet with the Azure Free Trial.
An Office 365 E5 Trial Subscription, which expires 30 days from when you create it.
What you end up with is an IT or app development playground with which you can experiment with Office 365 E5 features, such as Advanced Security Management. For example, you can:

Gain skills and experience in configuration and deployment
Create demos for your departments or customers
Test a complex configuration prior to implementing it in production
Install and test an Office 365 application running on APP1
You sign-in and access your Office 365 trial subscription from CLIENT1, which itself is accessed through a Remote Desktop connection. A natural question to ask here is: Why bother creating the corp.contoso.com intranet when I can access the trial subscription from my primary computer?

The advantage is that you can install modules and other software without consequence to your primary computer. Additionally, signing in from CLIENT1 means you won’t have conflicting sign-on credentials with your primary computer’s browser.

Another good reason is that we plan to extend this environment to include Azure AD Connect to perform DirSync with password sync with your Office 365 trial subscription. This is not something you should necessarily do with your organization’s on-premises Windows Server AD.

If there is a specific configuration or feature that you would like to see built on top of this basic infrastructure, please let us know at caab@microsoft.com.

