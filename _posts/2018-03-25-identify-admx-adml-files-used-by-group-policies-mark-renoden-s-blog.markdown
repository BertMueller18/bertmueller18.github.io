---
layout: post 
title:  "Identify ADMX/ADML Files used by Group Policies – Mark Renoden’s Blog" 
date:   2018-03-25T15:01:32.345Z 
categories: gpo powershell activedirecotry reporting
link: https://blogs.technet.microsoft.com/markrenoden/2018/01/11/identify-admxadml-files-used-by-group-policies/ 
tags:
  - links
ogtype: article 
---

## Identify ADMX/ADML Files used by Group Policies

### The Problem

Group Policy ADMX versioning has caused a few concerns for Microsoft customers in the past one to two years. A great description of the issue and how to address it is found here.

Recently, one of my customers wanted to identify the ADMX files referenced by Group Policies deployed in their domain so that they could carefully update the ADMX/ADML central store in SYSVOL. This isn't entirely easy because the ADMX file is not used when the GPO is applied to a computer or user.

Further Explanation

The ADMX/ADML file combination may be thought of as the description language that instructs the Group Policy editor. The Group Policy editor shows the policy settings, policy descriptions, drop down boxes and radio buttons that the ADMX/ADML files tell it to. Configuring a policy setting results in the Group Policy editor making changes to a .pol (or other) file in SYSVOL that is ultimately applied to the computer or user.

When you generate a Group Policy report, all of the ADMX and ADML files are read and compared with the policy settings stored in SYSVOL. This information is then glued together by the report generator and output as either HTML or XML. No record of the ADML/ADML files required for the report is kept.