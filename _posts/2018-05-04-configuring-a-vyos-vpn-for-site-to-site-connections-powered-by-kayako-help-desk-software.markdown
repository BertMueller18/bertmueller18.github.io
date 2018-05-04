---
layout: post 
title:  "Configuring a VyOS VPN for Site to Site Connections  - Powered by Kayako Help Desk Software" 
date:   2018-05-04T12:30:14.385Z 
categories: vyos networking vpn 
link: https://support.eapps.com/index.php?/Knowledgebase/Article/View/390/70/user-guide---vyos-vyatta-network-os-site-to-site-vpn 
tags:
  - links
ogtype: article 
---

## Configuring a VyOS VPN for Site to Site Connections
Posted by on 15 June 2017 04:30 PM
Applicable Plans - VyOS Network OS plans
VyOS (Vyatta) VPN Network Appliance - Site to Site VPN Configuration Guide
Overview

This is for our legacy VPN Appliance offering. For an updated guide using OPNsense, see https://support.eapps.com/vpn-appliance/site-to-site 
Vyatta VPN users: VyOS is the continuation of the open source Vyatta project, which is no longer available. VyOS is a drop-in replacement for Vyatta and functions in exactly the same manner. If you currently have Virtual Servers built with Vyatta Network OS, no changes will need to be made to your existing setup.

Using the VyOS Network OS (VPN Appliance) template, you can create a Virtual Server that acts as a network appliance that can function as an IPSEC compliant VPN, which will allow you to securely connect applications or services running on your Virtual Servers to applications or services running on remote servers (either on or off the eApps network). This is called a Site to Site VPN, and is documented in this User Guide.

	Make sure that you understand that a Virtual Server built with the VyOS Network OS (VPN Appliance) template will only function as a VPN or router network appliance. It will do nothing else. You cannot host websites on this VS, or use it as a mail server, or for any purpose other than as a VPN or router.
If you need assistance with your VyOS VPN, eApps offers a Professional Services option to help with the setup and configuration of your VPN. Our Technical Support team will work with you to determine your needs and put together a solution that meets your requirements. Please see our Professional Services page - eApps Professional Services or contact eApps Sales for more information.

Prerequisites