---
layout: post 
title:  "POWERSHELL: USE PARAMETERS AND CONFIGURATION FROM INI FILE, USE AS SPLATTING | vGeek - Tales from real IT system Administration environment" 
date:   2017-09-24T08:42:42.381Z 
categories: powershell programming splatting
link: http://www.vcloud-lab.com/entries/powershell/powershell-use-parameters-and-configuration-from-ini-file-use-as-splatting 
tags:
  - links
ogtype: article 
---

## POWERSHELL: USE PARAMETERS AND CONFIGURATION FROM INI FILE, USE AS SPLATTING
June 22, 2017 09:14PM
I was working on one of my friends requirement for automating scripts, He wanted a safe way to use parameters and configuration values from external file instead of modifying actual script, I tried with CSV as well as cliXML file. but found INI file is simple format as external plain text file to parse information from. Its very easy for any non-technical person to edit and review it. Before starting I would like to show the content of the INI file (schema). Same configuration I will be using in next Powershell splatting examples.

Text starting with ; semicolon are the comments and only for information purpose (description) and will be skipped while processing (This line is not necessary to mentioned in the file but it is best practice to document everything), next block is the configuration Name, enclosed with square brackets [], this is a main part I will be using to find related block for Syntax and parameter joined with equal = sign. In below file I have 3 parameter blocks for Service, Process and Folder as shown.