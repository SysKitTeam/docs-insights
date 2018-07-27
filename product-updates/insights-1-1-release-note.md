---
title: SysKit Insights 1.1.0 - Release Note
description: This article describes what's new and improved in the latest version of SysKit Insights.
author: Tomislav Sirovec
date: 23/7/2018
---

## Features

* Intra-farm Latency! We now check intra-farm Latency. During a 10-minute interval, we ping every server in the farm. According to [Microsoft’s guidelines]( https://docs.microsoft.com/en-us/sharepoint/install/hardware-and-software-requirements) 99.9% of pings must NOT take longer than 1 ms. If they do we will notify you. For detailed information about this feature, check out our [help article](#internal/get-to-know-insights/latency-screen).
* We heard your requests and now, entire SysKit Insights application is accessible via browser as a __web application__, making it easier than ever to share reports and event log searches with your colleagues. For more information on this, click [here].
* Event Viewer export - before, you could only export 1000 events to excel. This is now changed and you can specify the number of exportable events yourself.

## Improvements

* Regarding performance counters screen. It is now possible to disable the instance (hard drive) you do not wish to track. Furthermore, some hard drives (such as Witness drives) are hidden by default.	
* Alongside SharePoint Timer Service, now, you can also track SharePoint Search Service and SharePoint User Profile Service. If any of these services is stopped, we will notify you.
* Added SysKit Insights Maintenance service. Now, the Agent and the newly added Maintenance Service will start each other if one of them fails or is unexpectedly stopped. 
* On Manage Alerts form - Performance Counters section, you will now immediately see a __green dot__ if the __alerting__ for corresponding counter is enabled. 
* It is now possible to check the status of more than just one SharePoint site. Also, the site check URL must begin with htttp:// or https://.
* Added alerts and latency section to the Home Dashboard. 

## Bug Fixes

* Forwarded events had a delay in collection and thus the collection did not work properly. The issue is now fixed and the events can be accessed normally in the [Event Viewer](#internal/get-to-know-insights/event-viewer).
* Fixed an issue with ULS log collection if the ULS log path was not set to default. 
* Fixed a bug which caused Alerts form, to behave in an unexpected manner.
* Numerous smaller improvements and UI tweaks. 





