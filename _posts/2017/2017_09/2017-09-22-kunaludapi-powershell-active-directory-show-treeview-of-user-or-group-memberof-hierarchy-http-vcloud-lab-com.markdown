---
layout: post 
title:  "kunaludapi/Powershell-Active-Directory--Show-treeview-of-User-or-Group-memberof-hierarchy: http://vcloud-lab.com" 
date:   2017-09-22T17:27:06.794Z 
categories: activedirectory discovery documentation
link: https://github.com/kunaludapi/Powershell-Active-Directory--Show-treeview-of-User-or-Group-memberof-hierarchy 
tags:
  - links
ogtype: article 
---
## function Get-ADGroupTreeViewMemberOf
````powershell 
function Get-ADGroupTreeViewMemberOf {
#requires -version 4
<#
.SYNOPSIS
    Show UpStream tree view hierarchy of memberof groups recursively of a Active Directory user and Group.
.DESCRIPTION
    The Show-ADGroupTreeViewMemberOf list all nested group list of a AD user. It requires only valid parameter AD username, 
.PARAMETER UserName
    Prompts you valid active directory User name. You can use first character as an alias, If information is not provided it provides 'Administrator' user information. 
.PARAMETER GroupName
    Prompts you valid active directory Group name. You can use first character as an alias, If information is not provided it provides 'Domain Admins' group[ information.
.INPUTS
    Microsoft.ActiveDirectory.Management.ADUser
.OUTPUTS
    Microsoft.ActiveDirectory.Management.ADGroup
.NOTES
    Version:        1.0
    Author:         Kunal Udapi
    Creation Date:  10 September 2017
    Purpose/Change: Get the exact nested group info of user
    Useful URLs: http://vcloud-lab.com
.EXAMPLE
    PS C:\>.\Get-ADGroupTreeViewMemberOf -UserName Administrator

    This list all the upstream memberof group of an user.
.EXAMPLE
    PS C:\>.\Get-ADGroupTreeViewMemberOf -GroupName DomainAdmins

    This list all the upstream memberof group of a Group.
#>
````