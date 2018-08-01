---
title: SysKit Insights Performance 
description: Detailed overview on how to set up SysKit Insights to use HTTPS.
author: Hrvoje Bagarić
date: 28/07/2018
---

# Set up SysKit Insights to use HTTPS

There are a couple of steps needed to set up the SysKit Insights Web Application to use HTTPS instead of HTTP. If there are multiple agents connected to the same database, the following steps need to be performed on all the servers where SysKit Insights is installed:

1. Set up SysKit Insights
2. Set up URL reservation 

## 1. Setup SysKit Insights

The first thing to do is to stop both SysKit Insights Agent and SysKit Insights Maintenance Job in the Windows Services window on a server where SysKit Insights is installed. After both services are stopped (SysKit Insights Agent can take some time to stop), the file at %ProgramData%/SysKit/Insights/Service/settings.xml has to be modified. Using any text editor, set tag “SslEnabled” to “true.” After modifying the file, there needs to be the following tag in the file:
```xml
<SslEnabled>true</SslEnabled>
```
This setting will configure SysKit Insights to serve its web application over HTTPS.

## 2. Set up URL reservation

In order to set up SysKit Insights to serve content over HTTPS, users have to manually generate an SSL certificate. Using a self-signed certificate is not recommended and will not work on client machines unless those certificates are added to the trusted list of certificates on the client machines.

Once the certificate is obtained, it has to be installed to the Trusted Root Certification Authorities on the server that is hosting the SysKit Insights web application.

After the certificate is installed, users need to execute the following commands (the command prompt or PowerShell shell has to be open with the local administrator account):
```
C:\> netsh http add urlacl url=https://+:{insightsPort}/ user=Everyone
C:\> netsh http add sslcert ipport=0.0.0.0:{insightsPort} certhash={certificate hash} appid='{{unique guid}}'
``` 