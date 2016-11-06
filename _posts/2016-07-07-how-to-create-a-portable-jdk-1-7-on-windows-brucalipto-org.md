---
layout: post 
published: true 
title: "How to create a portable JDK 1.7 on windows" 
date: 2016-07-07T12:52:49.855Z 
link: http://www.brucalipto.org/java/how-to-create-a-portable-jdk-1-dot-7-on-windows/ 
tags: java
  - links
ogtype: article 
bodyclass: post 
---

> As a Java developer sometimes I need a version of Java Development Kit (JDK) that is not the one installed on my PC. Oracle Java installer on Windows does too many things that I cannot control (like changing the JVM used by browsers to run applets). As of this writing Java 7 is at version u45 and you can download it from here. Open the downloaded file with 7-zip (in my case was jdk-7u45-windows-i586.exe) and then open the tools.zip you find inside. Extract everything to a convenient path like C:\jdk-1.7u45. Now it is shell time so open a DOS console (Start->Run…->cmd) and type:

Create a portable JDK 1.7