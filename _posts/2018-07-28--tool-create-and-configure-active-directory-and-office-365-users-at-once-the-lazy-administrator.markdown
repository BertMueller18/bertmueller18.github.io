---
layout: post 
title:  "[Tool] Create and Configure Active Directory and Office 365 Users at Once. – The Lazy Administrator" 
date:   2018-07-28T16:54:27.900Z 
categories: powershell automation o365 
link: http://thelazyadministrator.com/2018/07/11/tool-create-and-configure-active-directory-and-office-365-users-at-once/ 
tags:
  - links
ogtype: article 
---

## [TOOL] CREATE AND CONFIGURE ACTIVE DIRECTORY AND OFFICE 365 USERS AT ONCE.
 July 11, 2018  Brad Wyatt Comments  3 Comments

One of the things IT Administrators look to automate first is the new user creation process. I recently was going through the process of creating a new hires Active Directory login, Office 365 mailbox, and their Office 365 user account, and I wondered how I could make the process easier and quicker.

My focus was geared towards Managed Service Providers (MSP’s), Human Resource (HR) departments and general Help Desk Technicians. For MSP’s I wanted to create a tool that they could easily use across all of their clients because they may not spend the time to automate new user creations because they have hundreds, if not thousands of clients to tend to, and each client is unique so you can’t just copy the same automation script from one client to another. This would also be a huge asset for Help Desk technicians because they are more often than not the ones creating new users. This would speed up the entire process of making new hires AD logins as well as their Office 365 accounts. Lastly, I wanted to make a tool that was incredibly easy to use that it can be given to an HR department so they can create new users and Office 365 mailboxes without ever having to contact the IT department at all.

I also wanted to be able to have the option of creating just an Active Directory user, just an Office 365 user, or both.

When making a new user in Active Directory Users and Computers you can enter the following information:

First name
Initials
Last name
Full name
User logon name

Active Directory Users and Computers new User wizard
If you want to enter items like E-Mail, password, group permissions, login scripts, home drive, etc. you would have to complete the new user wizard, find and then edit your user in Active Directory, and then fill in the necessary information. But what if we could enter all that information during the user creation process? We could add the user to groups, give them profile information, address, company info, enable multi-factor authentication and more, all without having to leave the new user wizard.