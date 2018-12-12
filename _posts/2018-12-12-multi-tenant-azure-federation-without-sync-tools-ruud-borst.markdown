---
layout: post 
title:  "Multi-tenant Azure federation without sync tools - Ruud Borst" 
date:   2018-12-12T11:05:01.764Z 
categories: azuread azure o365 powershell
link: http://www.ruudborst.nl/multi-tenant-azure-federation-without-dirsync-aadsync-aadconnect-fim/ 
tags:
  - links
ogtype: article 
---

> Multi-tenant Azure AD federation without the use of synchronization tools
Active Directory, ADFS, Azure, FrontPage, Office 365, PowerShell
Update: Added a multi-tenant PowerShell provisioning script to the TechNet gallery with examples mentioned in this blog. Download here.

Introduction

Microsoft is advocating their own synchronization tools (DirSync/AADSync/AADconnect/FIM) to federate with Azure AD. There are a lot of advantages using a synchronization tool, this way companies don’t need to develop their own solutions, it’s easy deployable, has a lot of out-of-the-box two way sync options and pretty much the way to go for most companies. These tools are mainly used for AD synchronisation with Office365 using Azure AD and built for one tenant businesses only. But demand for on-premise mult-tenancy support is growing, that’s because Microsoft recently begun actively onboarding larger companies and Cloud Providers into their Microsoft Cloud Solution Provider (CSP) program and of course the ever growing cloud adoption. These larger companies may have other requirements before they are ready to onboard their own customers or departments with Office 365 and Azure. One of these requirements may be leaving the authentication and objects on-premise, this could be because of company policy enforcing them to manage multifactor, audit or password authentication policies in their own cloud. Or they just want to leave their customers in their own directory for a variety of well-founded reasons like investments in own infrastructure, single sign-on, security, trust, regulation or legal issues.

In this federated scenario the authentication of federated user identities in Azure are redirected to the ADFS servers belonging to the company’s own AD. By using their own directory as the authentication and synchronization source they are also able to combine or cross-sell not only Office 365 services but also other federation ready services like Google+, SalesForce etc. And since they are hosting multiple customers or tenants a multi-tenant solution is key to their success and that’s precisely what is not yet available in any Microsoft synchronization tool. But luckily Microsoft or do I have to say Azure made federation functionality available in Azure PowerShell and in the Azure AD Graph API.  But there is a catch, if you want to implement the whole federation package then you have to do your research and development and do a lot of testing to make it compatible with your environment. I didn’t find a source yet where all the multitenant federation pieces came together, so I hope to solve the puzzle here if you’re going for the PowerShell way. This solution allows you to onboard your multitenant AD environment to a multitenant Azure AD environment, provisioning multiple tenants with multiple federated domains across multiple subscriptions.