---
layout: post 
title:  "URL Rewrite (redirect) of HTTP to HTTPS with Powershell script | A Geeks World" 
date:   2017-06-15T09:00:17.589Z 
categories: powershell iis deployment
link: http://www.isolation.se/url-rewrite-redirect-of-http-to-https-with-powershell-script/ 
tags:
  - links
ogtype: article 
---

> URL Rewrite (redirect) of HTTP to HTTPS with Powershell script

When deploying Web Application Proxy as a frontend to for example ADFS and Windows Azure Pack, or other services, the current version of Web AppProxy only supports HTTPS urls. It’s possible to use the “URL Rewrite” module for IIS to redirect users from HTTP to HTTPS. There are plenty of guides on internet on how to do that.
But I wanted to add that configuration to my WebApplication Proxy configuration script, and couldn’t find any powershell examples, so here is the script I’ve made.

It will use Web Platform installer to install the URL Rewrite module, then add the IIS Web Management tools, and in the end create a Global Rule redirecting all HTTP requests to HTTPS without the user noticing it.