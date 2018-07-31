---
title: SysKit Insights Performance 
description: Detailed overview on how the SysKit Insights collects and presents farm performance data.
author: Hrvoje Bagarić
date: 28/07/2018
---

# Set up SysKit Insights to use HTTPS

There are couple of steps needed to setup SysKit Insights Web Appliction to use HTTPS insted of HTTP. If there are multiple agents connected to the same database, all the servers where SysKit Insights is installed have to have following steps need to be performend:

1. Setup SysKit Insights
2. Set up URL reservation 

## 1. Setup SysKit Insights

First thing to do is to stop both SysKit Insights Agent and SysKit Insights Maintanance Job in Windows Services window on server where SysKit Insights is installed. After both services are stopped (SysKit Insights Agent can take some time to stop) the file at %ProgramData%/SysKit/Insights/Service/settings.xml have to be modified. Using any text editor, set tag 'SslEnabled' to true. After modifying file there needs to be follwing tag in the file:
```xml
<SslEnabled>true</SslEnabled>
```

This setting will configure SysKit Insights to serve its web application over HTTPS.

## 2. Set up URL reservation

In order to set up the SysKit Insights to serve content over the HTTPS, users have to manually generate SSL certificate. Using self-signed certificate is not recommended and will not work on client machines unless those certificates are added to the trusted list of certificates on client machines.

Once the certificate is obtained, it has to be installed to the Trusted Root Certification Authorities on server that is hosting SysKit Insights web application.

After the certificate is installed, users need to execute following commands (the command prompt or PowerShell shell have to be open with the local administrator account)
```
C:\> netsh http add urlacl url=https://+:{insightsPort}/ user=Everyone
C:\> netsh http add sslcert ipport=0.0.0.0:{insightsPort} certhash={certificate hash} appid={{unique guid}}
```