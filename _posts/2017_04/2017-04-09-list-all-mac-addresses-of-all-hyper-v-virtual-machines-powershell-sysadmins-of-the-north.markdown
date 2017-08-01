---
layout: post 
title:  "List all MAC addresses of all Hyper-V Virtual Machines - PowerShell - Sysadmins of the North" 
date:   2017-04-09T08:43:12.212Z 
categories: hyper-v powershell
link: https://www.saotn.org/list-mac-addresses-hyper-v-virtual-machines/ 
tags:
  - links
ogtype: article 
---

> How to list all MAC address of all VM’s on Hyper-V #

This tip shows you how to list MAC addresses on local or remote Hyper-V servers.

Advertisement:
A media access control address (MAC address) of a computer is a unique identifier assigned to network interfaces for communications at the data link layer of a network segment. MAC addresses are used as a network address for most IEEE 802 network technologies, including Ethernet and WiFi. Logically, MAC addresses are used in the media access control protocol sublayer of the OSI reference model.

– Wikipedia
A MAC address can be assigned manually by you, or automatically by Hyper-V. If you ever need to list all MAC addresses, use the Get-VM and Get-VMNetworkAdapter PowerShell cmdlets as shown in the following example:

On your local Hyper-V host, list the MAC addresses of all virtual machines (VM’s):

Get-VM | Get-VMNetworkAdapter | ft VMName, MacAddress
List MAC addresses of all virtual machines on all Hyper-V servers, run the following code in your PowerShell console:

$HypervServers = @("HyperV-01", "HyperV-02", "HyperV-03")
foreach ($HypervServer in $HypervServers) {
  Get-VM -Computername $HyperVServer | Get-VMNetworkAdapter | ft VMName, MacAddress
}
Or on a per remote Hyper-V server basis, run:

Get-VM -Computername hyper-v_server | Get-VMNetworkAdapter | ft VMName, MacAddress