---
layout: post 
title:  "SDDL ACL Syntax" 
date:   2017-03-31T19:35:11.840Z 
categories: activedirectory security sddl
link: https://msdn.microsoft.com/en-us/library/cc230374.aspx 
tags:
  - links
ogtype: article 
---

## SDDL Syntax

An SDDL string is a single sequence of characters. The format can be ANSI or Unicode; the actual protocol MUST specify the character set that is used. Regardless of the character set used, the characters that can be used are alphanumeric and punctuation.
The format for an SDDL string is described by the following ABNF (as specified in [RFC5234]) grammar, where the elements are as shown here.