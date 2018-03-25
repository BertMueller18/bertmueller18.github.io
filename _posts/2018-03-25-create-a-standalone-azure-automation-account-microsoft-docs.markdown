---
layout: post 
title:  "Create a standalone Azure Automation account | Microsoft Docs" 
date:   2018-03-25T15:19:14.376Z 
categories: azure powershell powershelldsc automation
link: https://docs.microsoft.com/en-us/azure/automation/automation-create-standalone-account 
tags:
  - links
ogtype: article 
---

## Create a standalone Azure Automation account
03/15/2018
5 minutes to read
Contributors
      
This article shows you how to create an Azure Automation account in the Azure portal. You can use the portal Automation account to evaluate and learn about Automation without using additional management solutions or integration with Azure Log Analytics. You can add those management solutions or integrate with Log Analytics for advanced monitoring of runbook jobs at any point in the future.

With an Automation account, you can authenticate runbooks by managing resources in either Azure Resource Manager or the classic deployment model.

When you create an Automation account in the Azure portal, these accounts are automatically created:

Run As account. This account does the following tasks:
Creates a service principal in Azure Active Directory (Azure AD).
Creates a certificate.
Assigns the Contributor Role-Based Access Control (RBAC), which manages Azure Resource Manager resources by using runbooks.
Classic Run As account. This account uploads a management certificate. The certificate manages classic resources by using runbooks.
With these accounts created for you, you can quickly start building and deploying runbooks to support your automation needs.

