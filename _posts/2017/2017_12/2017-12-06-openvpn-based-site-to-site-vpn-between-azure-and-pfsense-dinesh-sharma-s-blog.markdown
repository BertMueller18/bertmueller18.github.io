---
layout: post 
title:  "OpenVPN based Site-to-Site VPN between Azure and pfSense - Dinesh Sharma's Blog" 
date:   2017-12-06T22:26:38.319Z 
categories: openvpn azure pfsense site2site
link: http://www.dscentral.in/2017/02/10/s2s-vpn-azure-pfsense-openvpn/ 
tags:
  - links
ogtype: article 
---

# OpenVPN based Site-to-Site VPN between Azure and pfSense

FEBRUARY 10, 2017 BY DINESH SHARMA 0 COMMENTS

In Azure terminology, a Site-to-Site (S2S) VPN is a VPN connection between two gateway devices. It allows communication between subnets on-prem and in an Azure virtual network. Gateway devices on-prem are usually firewalls, like pfSense in this post. In Azure, we can use Azure VPN gateway or we can set up our own virtual appliance for this purpose. A virtual appliance is nothing but a VM that can provide such security and filtering services.

OpenVPN Use Case

Azure VPN Gateway uses IKE/IPSEC. It requires a static public IP on the on-prem device. Officially, it does not support the device behind NAT but works if you forward UDP ports 500 and 4500 (NAT-T). It only supports one S2S tunnel/site when using PolicyBased VPN. Most open source firewalls only support PolicyBased VPNs.

On the other hand, OpenVPN is an SSL VPN and does not need any port forwarding on-prem. Public IP on-prem can be dynamic. It works even if the device is behind NAT or even double NAT, which is the case of cable network ISPs. OpenVPN client endpoint can also be configured on a Windows server if your firewall doesn’t support it natively.

In short, OpenVPN can provide a most compatible solution which can be very helpful when setting up hybrid labs.