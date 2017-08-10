---
layout: post 
title:  "Why I love the PowerShell AppDeployment Toolkit – Sinisa Sokolic" 
date:   2017-06-22T22:15:35.106Z 
categories: deployment mdt powershell psadt 
link: https://www.sinisasokolic.com/why-i-love-the-powershell-appdeployment-toolkit/ 
tags:
  - links
ogtype: article 
---

## Why I love the PowerShell AppDeployment Toolkit

Today I want to share some thoughts and insights about a very useful toolkit that is available free for everybody – The PowerShell App Deployment Toolkit. I will describe what features it has, how the architecture looks like and how you can create and customize packages. At the end I will provide you with some packages you can start to play with.

First I want to make a short excurse about wrappers.

About Wrappers…

A wrapper is basically a script that runs certain functions around an installation package. This scripts could for example run copy jobs before or after the installation routine of an application, clean up files or provide extended logging functionality that some electronic software delivery products are missing today. In short: It provides functionality that is not available in an ESD product from scratch.

About wrapper languages…

Most of the wrappers in the field are still written in VBScript or as a Batch and although VBS is very fast and efficient I personally don´t like the fact that is not as easy to understand as a PowerShell script. Therefore the PSADK is IMHO the better wrapper.

About The PowerShell App Deployment Toolkit

The PowerShell App Deployment Toolkit was launched in August 2013 and is a joint collaboration between Seán Lillis and Dan Cunningham. Muhammad Mashwani and Aman Motazedian. You can use it for whatever deployment mechanism or ESD you are using in your infrastructure. It is written completely in PowerShell and has a lot of functions around deploying applications to endpoints and users. It is licensed under the Microsoft Public License (Ms-PL). See some of the features in the following list: