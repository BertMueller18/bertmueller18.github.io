---
layout: post 
title:  "Recompiling Chocolatey packages - WinSysBlog" 
date:   2017-09-30T09:10:01.171Z 
categories: 
tags:
  - links
ogtype: article 
---

> Recompiling Chocolatey packages
Published by Dan Franciscus on August 2, 2017

Chocolatey is a very popular tool among system administrators as it helps automate package management for Windows. Since Chocolatey can be used completely with a CLI, you can programmatically create, install and uninstall packages locally and remotely. One of the main issues I normally hear from Chocolatey users is that they do not trust to install packages directly from the main Chocolatey public repository. This is for good reason since in order to trust the repository you must trust whoever is maintaining that package and there is only so much vetting Chocolatey can do to ensure a package is safe. Not to mention if you use the public repository exclusively as your source of packages you are constantly downloaded packages from the internet which leads to additional security concerns.

One feature of Chocolatey Business I enjoy is the capability to recompile packages hosted on its public repository and internalize them so they can be deployed from on your own NuGet server. During this process Chocolatey downloads the NuGet package and changes its code so that all resources needed are now on your NuGet server.

