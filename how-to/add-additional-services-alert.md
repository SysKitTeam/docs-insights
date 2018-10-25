---
title: Add custom Services alert
description: This article explains how to add a custom Service alert to the application. 
author: Tomislav Sirovec
date: 28/9/2018
--- 

If you wish to __track additional services__, this article explains how to add a custom Service alert into the application.  
Run the following script against the SysKit Insights database.

```sql
INSERT INTO [Alerts].[AlertDefinitions] (FarmId, Name, IgnorePeriod, Type, Configuration, Enabled, SendToDefaultEmail, SendToAdditionalEmails, AdditionalEmailRecipients)
SELECT Farm.ID,
   '{AlertName}',
   30,
   1,
   '<SearchServiceCheckConfig xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://schemas.datacontract.org/2004/07/SysKit.Insights.Application.Alerting.CreateConfigurations">
       <ServiceNameToCheck> -SERVICE NAME HERE- </ServiceNameToCheck>
   </SearchServiceCheckConfig>',
   1,
   1,
   0,
   ''
From [dbo].[Farms] as Farm
WHERE Farm.Name = {FarmName}
```

Replace the properties in curly brackets (AlertName and FarmName) and input the Service name you wish to start tracking. Most common request we have been receiving is to add a Workflow Manager Service. In that case you would input: WorkflowServiceBackend as that is the __service name.__ 

If you require more assistance with this issue, don't hesitate to [ask us.](https://www.syskit.com/company/contact-us/)