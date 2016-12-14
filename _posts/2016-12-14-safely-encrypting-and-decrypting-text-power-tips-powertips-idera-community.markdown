---
layout: post 
title:  "Safely Encrypting and Decrypting Text - Power Tips - PowerTips - IDERA Community" 
date:   2016-12-14T10:28:28.246Z 
categories: powershell programming
link: http://community.idera.com/powershell/powertips/b/tips/posts/safely-encrypting-and-decrypting-text?utm_content=bufferdb512&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer 
tags:
  - links
ogtype: article 
---

> Safely Encrypting and Decrypting Text

When you encrypt secret information, the challenge is to find a good secret. One particular safe secret would be your Windows identity, paired with your computer’s identity. This can be used to encrypt sensitive personal information on a particular computer.

Here are two functions that illustrate how it’s done:

function Decrypt-Text
{
  
  param
  (
    [String]
    [Parameter(Mandatory,ValueFromPipeline)]
    $EncryptedText
  )
  process
  {
    $secureString = $EncryptedText | ConvertTo-SecureString
    $BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secureString)
    [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
  }
}

function Encrypt-Text
{
  
  param
  (
    [String]
    [Parameter(Mandatory,ValueFromPipeline)]
    $Text
  )
  process
  {
     $Text | 
       ConvertTo-SecureString -AsPlainText -Force | 
       ConvertFrom-SecureString
  }
}

'PowerShell Rocks' | Encrypt-Text 
'Hello, World!' | Encrypt-Text | Decrypt-Text
You can safely save the encrypted text to a file. Only you will be able to read in and decrypt that text again, and only if it is done on the computer used to encrypt the data.