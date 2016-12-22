---
layout: post 
published: true 
title: "Lab: Part 22 – Ultimate StoreFront 3 customization guide | Citrix Guru" 
date: 2016-08-29T03:48:37.534Z
categories: storefront citrix
link: http://www.citrixguru.com/2016/03/08/lab-ultimate-storefront-customization-guide/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Lab: Part 22 – Ultimate StoreFront 3 customization guide


Nicolas ignoto | On 08, Mar 2016

Rate this post



Customize your Citrix StoreFront 3 website.

Make sure to catch up this series' previous posts first!

Building a Dual-Xeon Citrix Lab: Part 1 – Considerations
Building a Dual-Xeon Citrix Lab: Part 2 – Hardware
Building a Dual-Xeon Citrix Lab: Part 3 – Windows and Hyper-V installation
Lab: Part 4 – Hyper-V Networking
Lab: Part 5 – NetScaler 11 Architecture and Installation
Lab: Part 6 – Configure NetScaler 11 High Availability (HA Pair)
Lab: Part 7 – Upgrade NetScalers in HA
Lab: Part 8 – Save, Backup and Restore NetScaler 11 configuration
Lab: Part 9 – Install Microsoft SQL Server 2014 (Dedicated)
Lab: Part 10 – Citrix Licensing demystified
Lab: Part 11 – Install XenDesktop 7.6
Lab: Part 12 – Setup NetScaler 11 Clustering (TriScale)
Lab: Part 13 – Configure Published Applications with XenDesktop 7.6
Lab: Part 14 – Citrix StoreFront 3.x
Lab: Part 15 – Configure SSL in StoreFront
Lab: Part 16 – StoreFront load balancing with NetScaler (Internal)
Lab: Part 17 – Optimize and secure StoreFront load balancing with NetScaler (Internal)
Lab: Part 18 – Secure LDAP (LDAPS) load balancing with Citrix NetScaler 11
Lab: Part 19 – Configure Active Directory authentication(LDAP) with Citrix NetScaler 11
Lab: Part 20 – RDP Proxy with NetScaler Unified Gateway 11
Lab: Part 21 – Secure SSH Authentication with NetScaler (public-private key pair)
Lab: Part 22 – Ultimate StoreFront 3 customization guide
Lab: Part 23 – Securing Citrix StoreFront DMZ deployment
 
Getting Started

Only do changes in the configuration files located in the StoreFront custom folder. This will help you during StoreFront upgrades as the content from the custom folder will remain.
Default location:
Javascript -> C:\inetpub\wwwroot\Citrix\<StoreName>Web\custom\script.js
CSS -> C:\inetpub\wwwroot\Citrix\<StoreName>Web\custom\style.css
Copy new images in C:\inetpub\wwwroot\Citrix\<StoreName>Web\custom\
Progagate your changes to all secondary servers using the StoreFront propagation feature or copy the content of the custom folder to all the servers.
Troubleshooting:
Display alerts: http://<StoreFrontURL/Citrix/<StoreName>Web/#-errors
Enable debug: http://<StoreFrontURL/Citrix/<StoreName>Web/#-debug
Disable customizations: http://<StoreFrontURL/Citrix/<StoreName>Web/#-nocustom
Enable tracing: http://<StoreFrontURL/Citrix/<StoreName>Web/#-tr
Enable tracing with no customizations: http://<StoreFrontURL/Citrix/<StoreName>Web/#-tr-nocustom
