---
description: Detailed overview on how to set up Syskit Insights to use HTTPS.
---

# Set up HTTPS

There are a couple of steps needed to set up the Syskit Insights Web Application to use HTTPS instead of HTTP. If there are multiple agents connected to the same database, the following steps need to be performed on all the servers where Syskit Insights is installed:

1. Set up Syskit Insights
2. Set up URL reservation 

## 1. Setup Syskit Insights

The first thing to do is to stop both Syskit Insights Agent and Syskit Insights Maintenance Job in the Windows Services window on a server where Syskit Insights is installed. After both services are stopped \(Syskit Insights Agent can take some time to stop\), the file at %ProgramData%/SysKit/Insights/Service/settings.xml has to be modified. Using any text editor, set tag “SslEnabled” to “true”. After modifying the file, there needs to be the following tag in the file:

```markup
<SslEnabled>true</SslEnabled>
```

This setting will configure Syskit Insights to serve its web application over HTTPS.

## 2. Set up URL reservation

In order to set up Syskit Insights to serve content over HTTPS, users have to manually generate an SSL certificate. Using a self-signed certificate is not recommended and will not work on client machines unless those certificates are added to the trusted list of certificates on the client machines.

Once the certificate is obtained, it has to be installed to the Trusted Root Certification Authorities on the server that is hosting the Syskit Insights web application.

After the certificate is installed, users need to execute the following commands \(the command prompt or PowerShell shell has to be open with the local administrator account\):

```text
C:\> netsh http add urlacl url=https://+:{insightsPort}/ user=Everyone
C:\> netsh http add sslcert ipport=0.0.0.0:{insightsPort} certhash={certificate hash} appid='{{unique guid}}'
```

## 3. Update SysKitInsights database

Lastly, hostname in SyskitInsights database must be updated.

The following SQL query should be executed:

```
/****** CHANGE VALUES FOR {NewHostname} AND {OldHostname} BEFORE RUNNING THE SCRIPT ******/
UPDATE [EventCollection].[Agents]
   SET [HostName] = '{NewHostname}'
 WHERE [HostName] = '{OldHostname}'
```

**Note:** When using HTTPS, Syskit Insights requires you to confirm the agent URL on each startup. If no changes were made, click the Set button, and you are good to go.

