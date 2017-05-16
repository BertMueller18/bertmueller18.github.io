---
layout: post 
title:  "Managing Inbox Rules in Exchange Server 2010 - TechGenix" 
date:   2017-05-16T21:32:49.730Z 
categories: exchange exchange2013 exchange2013 inboxrule
link: http://techgenix.com/managing-inbox-rules-exchange-server-2010/ 
tags:
  - links
ogtype: article 
---

## Managing Inbox Rules in Exchange Server 2010

Introduction

As a consultant, I have witnessed several directors and managers saying that they have something wrong with their Inbox. As Exchange Administrators we know that the guy must have created a messed up Inbox rule, however, it is always Exchange who gets the blame!

If we had the ability to manage users’ Inbox rules without going to their machine it would save a lot of time for the Help Desk team. Through Inbox Rules, you can have an Internal Application that requires some actions that you would rather not have to explain to all your users, and you can create an Inbox Rule for that specific application for everyone without any trouble.

Okay, so far I gave you a couple of scenarios where the Inbox rule management can be a pain, but if you are using Exchange Server 2010 then you have an easy solution for all these dilemmas. We can use Exchange Management Shell and a couple of Inbox Rule cmdlets to perform all those tasks in a few seconds!

Long story short, we will be able to create, delete, disable, and change Inbox Rules using PowerShell without interacting with the end users.