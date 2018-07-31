---
title: SysKit Insights Performance 
description: Detailed overview on how the SysKit Insights collects and presents farm performance data.
author: Hrvoje Bagarić
date: 28/07/2018
---

## Set up SysKit Insights to use HTTPS

In order to set up the SysKit Insights to serve content over the HTTPS, users have to manually generate SSL certificate. Using self-signed certificate is not recommended and will not work on client machines unless those certificates are added to the trusted list of certificates on client machines.

Once the certificate is obtained, it has to be installed to the Trusted Root Certification Authorities on server that is hosting SysKit Insights web application.

After the certificate is installed, users need to execute following commands (the command prompt or PowerShell shell have to be open with the local administrator account)
```
C:\> netsh http add urlacl url=https://+:{insightsPort}/ user=Everyone
C:\> netsh http add sslcert ipport=0.0.0.0:{insightsPort} certhash={certificate hash} appid={{cretificate app id}}
```