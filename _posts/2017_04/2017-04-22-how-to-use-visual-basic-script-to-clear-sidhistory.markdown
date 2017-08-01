---
layout: post 
title:  "How To Use Visual Basic Script to Clear SidHistory" 
date:   2017-04-22T09:42:12.263Z 
categories: activedirectory security sid
link: https://support.microsoft.com/en-us/help/295758/how-to-use-visual-basic-script-to-clear-sidhistory 
tags:
  - links
ogtype: article 
---

> How To Use Visual Basic Script to Clear SidHistory
 Email
 Print
Summary
The Microsoft Visual Basic Script (VBScript) provided in this article will find an object by its name in the directory and attempt to clear the sidHistory for that object. It has optional parameters for objectClass and objectCategory to help in the search.
More Information
When a user object moves from one domain to another, a new security identifier (SID) must be generated for the user account and stored in the Object-SID property. Before the new value is written to the property, the previous value is copied to another property of a User object, SID-History (sidHistory). This property can hold multiple values. Each time a User object moves to another domain, a new SID is generated and stored in the Object-SID property and another value is added to the list of old SIDs in SID-History. Sometimes it may be necessary to clear the sidHistory.

The following VBScript code will remove the sidHistory attribute from the directory object specified in the command line arguments. 