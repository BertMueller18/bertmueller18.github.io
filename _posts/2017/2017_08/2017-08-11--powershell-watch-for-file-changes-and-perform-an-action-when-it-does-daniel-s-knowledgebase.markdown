---
layout: post 
title:  "[Powershell] – Watch for file changes and perform an action when it does | Daniel's Knowledgebase" 
date:   2017-08-11T07:31:20.265Z 
categories: powershell automation 
link: https://danielsknowledgebase.wordpress.com/2017/08/03/powershell-watch-for-file-changes-and-perform-an-action-when-it-does/ 
tags:
  - links
ogtype: article 
---

## [POWERSHELL] – WATCH FOR FILE CHANGES AND PERFORM AN ACTION WHEN IT DOES
As you might notice, I don’t really like to do the same procedure more than a few times if there is a way to automate it, and usually there is, so I investigate it for sure.
Currently, I’m working in a project that has deploying process that, although it’s simple, really annoyed me. Until I automated it 
The deployment is done to a Raspberry Pi with Raspbian lite (without user interface). The “problem” here is that the solution is developed and built in Windows and then sent to the Raspberry via FTP. As I said, the process is simple: Compile the solution, go to an FTP client (I’m using FileZilla for example), navigate to \solutionFolder\bin\release\ and copy the application.exe to the destination folder on the raspberry.
Here I’m talking about early state development, where I compile and test something like 20 times per hour for example.
Wouldn’t it be nice if there was a way to, whenever the solution is compiled, copy the application.exe to the raspberry automatically? Well, since I’ve already said that I investigate for automation and now I’m asking this, obviously you know the answer.