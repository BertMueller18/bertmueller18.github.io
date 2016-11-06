---
layout: post 
published: true 
title: "Easily Create a Hyper-V Windows Server 2016 AD &amp; Nano Server Lab | PowerShell, Programming and DevOps" 
date: 2016-10-23T13:46:15.015Z 
link: https://dscottraynsford.wordpress.com/2016/10/04/easily-create-a-hyper-v-windows-server-2016-ad-nano-server-lab/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Easily Create a Hyper-V Windows Server 2016 AD & Nano Server Lab

Introduction

One of the PowerShell Modules I’ve been working on for the last year is called LabBuilder.The goal of this module is:

To automatically build a multiple machine Hyper-V Lab environment from an XML configuration file and other optional installation scripts.

What this essentially does is allow you to easily build Lab environments using a specification file. All you need to do is provide the Hyper-V environment and the Operating System disk ISO files that will be used to build the lab. This is great for getting a Lab environment spun up for testing or training purposes.

Note: Building a new Lab can take a little while, depending on the number of VM’s in the Lab as well as the number of different Operating Systems used. For example, a Lab with 10 VMs could take an hour or two to spin up, depending on your hardware.