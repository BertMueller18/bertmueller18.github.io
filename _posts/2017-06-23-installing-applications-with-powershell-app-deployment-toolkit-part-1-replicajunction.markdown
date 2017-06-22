---
layout: post 
title:  "Installing Applications with PowerShell App Deployment Toolkit - Part 1 · replicaJunction" 
date:   2017-06-22T22:16:40.976Z 
categories: deployment mdt powershell psadt 
link: https://replicajunction.github.io/2015/04/07/installing-applications-with-psadt-part1/ 
tags:
  - links
ogtype: article 
---

> nstalling Applications with PowerShell App Deployment Toolkit - Part 1
04/07/15 on PowerShell, PSADT
Table of Contents
Table of Contents
Introduction
Getting Started
Downloading files
Preparing the environment
Building the Deployment Package
Defining some variables
A word on deployment modes
Running the Firefox setup file
Finding the silent path
Performing the install
Adding an uninstall
Troubleshooting
Deploying and Using the Package
Next Steps
This is Part 1 in a 2-part series.

Part 1
Part 2
Introduction
For over a year now, I’ve been the primary software administrator for our organization’s SCCM infrastructure. This means I’ve been responsible for integrating software installs in our workstation build process, but I’ve also had to deal with the issue of deploying and updating software on end-user workstations.

Administering software deployments presents a unique set of challenges: