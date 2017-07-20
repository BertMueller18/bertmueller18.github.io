---
layout: post 
title:  "Remote Server Management for Large Enterprises—Part One – IRONBRICK" 
date:   2017-07-20T22:21:58.162Z 
categories: powershell automation winrm remoting
link: http://www.ironbrick.com/remote-server-management-for-large-enterprises-part-one/ 
tags:
  - links
ogtype: article 
---

## Remote Server Management for Large Enterprises

### Part One

By Dheeraj Advani
Automation Engineer, IronBrick

During its relatively short life, Microsoft’s PowerShell has become a powerful tool for enterprise-wide server management. Most system administrators are familiar with the tool’s interface and may have even dabbled in running a few scripts to make their day-to-day activities easier. For an enterprise, it is important to recognize how we can leverage this tool to perform management activities across multiple machines.

One key advantage to using PowerShell remote management is the ability to write scripted code blocks and execute them against multiple servers in a single run. This allows us to enforce compliance with new configurations, optimizations, or even security policies across an entire enterprise on-demand. Due to the nature of remote PowerShell execution, it is easy to write and test a script on one machine and then place it inside another piece of code that will take that script and execute it across all machines in the environment. In this configuration, we suddenly gain the ability to manage as many servers as we would like with a minimal lag time for deployment. That is to say; this method has the potential for massive outward scalability which allows us to better respond to the growing needs of an ever-changing server landscape.

This IT Matters by IronBrick blog series has the goal of introducing the concepts you will need to remotely manage a large enterprise server deployment, as well as some information on pitfalls you may encounter along the way.

#### Step 1: Configuring a Server to Accept Remote Sessions

To set up both a source and destination server so they can accept remote PowerShell sessions, execute the following commands from an elevated PowerShell session:

 ````powershell
enable-psremoting
winrm quickconfig
set-item wsman:\localhost\client\trustedhosts *
winrm set winrm/config/winrs '@{MaxMemoryPerShellMB="2048"}'
restart-service winrm
 ````
 

These commands will give you the settings you need to remote into a machine using PowerShell. The parameter—MaxMemoryPerShellMB—sets the amount of RAM a remote session is able to use. Sometimes you will run into an unexplainable failure that occurs only during a remote execution of a script and is the result of maxing the memory allocation for the remote session. With these in place, we are ready to try a remote PowerShell session.

#### Step 2: Entering a PowerShell Session Using Domain Credentials

As Windows uses Kerberos authentication between machines on the same domain; we can leverage the security features built into Microsoft active directory to facilitate a secure connection.

To begin, we shall assume we have two machines: <Server1> and <Server2>. I want to execute a command remotely on <Server2> from <Server1>.



I will immediately be prompted for my domain credentials and when I enter them, the next prompt I see from PowerShell will be on the target server. However, when doing this against multiple machines, it becomes tedious to be prompted for and enter domain credentials every time. Let’s store the credentials for this session:



You will once again be prompted to enter your domain credentials. These will be stored in a secure variable—$Credentials—for the current session only. Now we can enter a remote session like this:



#### Step 3: Making Use of These Features

So, you’ve set up machines in your development environment and tried out all the PowerShell remoting options, written scripts, and executed them remotely. You are now ready to go into the real world in your large enterprise and roll out a configuration change against all the servers in a domain.

You kick off your PowerShell script which will iterate through all the servers. Although it is connecting to the first one, you will get an error:

The WinRM client cannot process the request. It cannot determine the content type of the HTTP response from the destination computer.

Well, that’s about the most generic error you could get, so you re-test the script against your development environment and everything checks out.

To understand this scenario we need to understand what is going on under the hood with PowerShell remoting. When I tell the machine to enter a session to a remote server, it will pass a Kerberos token with my credential information to the target machine. The target machine will ensure that I have the necessary access to open a remote session before allowing my session to open.

This is where the real world rears its ugly head. The Kerberos token contains all the information about your AD user account and, in large enterprises, can become quite bloated. If the frame containing the Kerberos token is larger than a value set on the target machine, it will immediately drop the session with the above error.

It doesn’t help that the default value for this attribute from Microsoft can be as low as 12Kb. Luckily, it’s an easy fix. You will need to add the following items to your registry on the target machine:

[Image New-Item](../images/new-item.jpg)

We have now covered the basics of PowerShell remoting, as well as some potential issues you can encounter going into production. In my next blog, I will explore the execution of remote scripts across the enterprise and show you how to iterate through a list of all the servers in your environment to execute scripts against them.

After all, in modern IT, the name of the game is agility.