---
layout: post 
title:  "HowTo: Create Self-Signed Certificates with PowerShell - David Christiansen" 
date:   2017-09-29T14:16:35.338Z 
categories: powershell certificate 
link: http://blog.davidchristiansen.com/2016/09/howto-create-self-signed-certificates-with-powershell/ 
tags:
  - links
ogtype: article 
---

> HowTo: Create Self-Signed Certificates with PowerShell
Posted on September 8, 2016
This is a short post about how to create Self-Signed certificates with the New-SelfSignedCertificate  PowerShell module.  More specifically, this post will cover creating your own Root Certificate, exporting public and PFX certificates, creating certificates signed by your root certificate authority.  Historically you would do this using the old-trusty makecert.exe, but nowadays we can do it straight from powershell! (oh joy!)


Create Root Certificate
Here’s what we are going to do:

Create the certificate;
Define a password string;
Export the certificate in PFX format, and secure it with the password you identified;
Export the public certificate and save it as a .cer file.
So let’s get going.  In your powershell console, type the following (Replacing the dnsname with something relevant to you)


1
New-SelfSignedCertificate -certstorelocation cert:\localmachine\my -dnsname "Lab Root Certificate Authority"
this will result in something along the line of the following being displayed in the console

Microsoft.PowerShell.Security\Certificate::LocalMachine\my

Thumbprint Subject
———- ——-
F81AFDC2A23B8629580374E64871941476E43F02 CN=DC Lab Root Authority

You want to take a note of the thumbprint guid displayed as you will need this later.  In the case above, the thumbprint is F81AFDC2A23B8629580374E64871941476E43F02

You then want to set up a variable a string value as the password


1
$pwd = ConvertTo-SecureString -String "Please-Use-A-Really-Strong-Password" -Force -AsPlainText
Now, let’s export the root certificate as a PFX file and use the password we just set up.


1
Export-PfxCertificate -cert cert:\localMachine\my\F81AFDC2A23B8629580374E64871941476E43F02  -FilePath root-authority.pfx -Password $pwd
Great, now you have the PFX file saved, let’s export the public key of your root authority (this is what you will install in “Trusted Root Authorities” for example).  NB: As it’s the only the public certificate we are exporting, you do not need to set a password.


1
Export-Certificate -Cert cert:\localMachine\my\F81AFDC2A23B8629580374E64871941476E43F02 -FilePath root-authority.crt
Create Certificates signed by our Root Certificate Authority

Here’s what we are going to do:

Load the root authority certificate into memory;
Create a certificate signed by the root authority;
Define a password string to secure the PFX file;
Export the new certificate as a PFX file;
Export the new certificate as a CRT file
Load the root authority certificate
Load the root authority certificate is as easy as pie.  Below I am using the root cert authority thumbprint discovered above


1
$rootcert = ( Get-ChildItem -Path cert:\LocalMachine\My\F81AFDC2A23B8629580374E64871941476E43F02 )
Create a certificate signed by the root authority

OK, so now we want to create a new certificate, but this time have the root certificate authority sign it.


1
New-SelfSignedCertificate -certstorelocation cert:\localmachine\my -dnsname "Gateway Certificate" -Signer $rootcert
nb: I am not using a resolvable dnsname in my example, but you can! (such as www.example.com)

This will result in the thumbprint of the new certificate being displayed in the console.  Again, record this thumbprint for use later.

Define a password string

1
$pwd2 = ConvertTo-SecureString -String "Please-Use-A-Really-Strong-Password" -Force -AsPlainText
Export the new certificate as a PFX file


1
Export-PfxCertificate -cert cert:\localMachine\my\A01F36FC2A7EB9CD506BD37E201935D6EB58A592  -FilePath gateway-certificate.pfx -Password $pwd2
Export new certificate public key as a CRT file

Use the following to export the public key of the certificate.


1
Export-Certificate -Cert cert:\localMachine\my\A01F36FC2A7EB9CD506BD37E201935D6EB58A592 -FilePath gateway.crt
All done !! No makecert.exe or mmc to be seen 

have fun.

DC

ps. For extra fun, here are some other examples

Extra: Create Certificates with Subject Alternative Names (SAN)
New-SelfSignedCertificate -DnsName domain.example.com,anothersubdomain.example.com -CertStoreLocation cert:\LocalMachine\My

Extra: Create Wildcard Certificates
New-SelfSignedCertificate -dnsname *.example.com -certstorelocation cert:\localmachine\my