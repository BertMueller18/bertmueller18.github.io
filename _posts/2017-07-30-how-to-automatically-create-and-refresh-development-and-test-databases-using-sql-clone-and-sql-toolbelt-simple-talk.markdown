---
layout: post 
title:  "How to Automatically Create and Refresh Development and Test Databases using SQL Clone and SQL Toolbelt - Simple Talk" 
date:   2017-07-29T22:33:39.048Z 
categories: sqlserver powershell 
link: https://www.red-gate.com/simple-talk/sql/database-delivery/automatically-create-refresh-development-test-databases-using-sql-clone-sql-toolbelt/ 
tags:
  - links
ogtype: article 
---

> How to Automatically Create and Refresh Development and Test Databases using SQL Clone and SQL Toolbelt
In order to be able to deliver database changes more quickly, there are several tasks that must be automated. It can be a daunting job to ensure that the whole team has the latest database build when there is a proliferation of copies, and the database is big. Phil illustrates a solution by taking a set of Redgate tools to show how they can be used together, via PowerShell, to build a database from object-level source, stock it with data, document it, and then provision any number of test and development servers with the database build, taking care to save any DDL changes to the existing copies of the database.
This article presents a PowerShell automation script that creates and refreshes the various databases on one or more servers that are required for test and development work, It uses Redgate’s SQL Clone, SQL Compare and a few other optional tools from the SQL Toolbelt.

A basic premise of this solution is that a database is being developed, and its source is stored in the version control system (VCS). The automation script will build the database from the latest build script in version control, stock it with data if wanted, and document the database if required. In the next stage, it uses SQL Clone to create an image of this database, and from the image it creates create ‘clones’ of the database, or refreshes existing clones, on each of the SQL Server development and test instances that you specify. The net result is that all the development and test databases should end up with metadata and data that is identical to that specified in the source, for that database version.

The automation script comes with a few safety checks to ensure, for example, that before dropping existing clones and creating new ones from a new image, any changes to local database clones are written to a directory in the VCS as a safeguard.

