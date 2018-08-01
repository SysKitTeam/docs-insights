---
title: SysKit Insights 1.1.0 - Release Note
description: This article describes what’s new and improved in the latest version of SysKit Insights.
author: Tomislav Sirovec
date: 23/7/2018
---

## Features

* Intra-farm latency! We now check intra-farm latency. In 10-minute intervals, we ping every server in the farm. According to [Microsoft’s hardware requirements](https://docs.microsoft.com/en-us/sharepoint/install/hardware-and-software-requirements), 99.9% of pings must be under 1 ms. If they’re not, we will notify you. For detailed information about this feature, check out our [help article](#internal/get-to-know-insights/latency-screen).
* We heard your requests, and now the entire SysKit Insights application is accessible via browser as a __web application__, making it easier than ever to share reports and event log searches with your colleagues. For more information, click [here](#internal/get-to-know-insights/web-application).
* Event Viewer export: Previously, you could only export 1,000 events to Excel. You can now specify the number of exportable events.

## Improvements

* In the performance counters screen, it is now possible to disable the instance (hard drive) you do not wish to track. Furthermore, some hard drives (such as Witness drives) are hidden by default.
* Alongside SharePoint Timer Service, you can now also track SharePoint Search Service and SharePoint User Profile Service. If any of these services is stopped, we will notify you.
* We’ve added SysKit Insights Maintenance service. Now, the Agent and the newly added Maintenance Service will start each other if one of them fails or is unexpectedly stopped.
* In the Manage Alerts form – Performance Counters section, you will now immediately see a __green dot__ if __alerting__ for the corresponding counter is enabled.
* It is now possible to check the status of more than just one SharePoint site. Also, the site check URL must begin with htttp:// or https://. 
* We’ve added alerts and latency sections to the Home Dashboard. 

## Bug Fixes

* Forwarded events had a delay in collection; thus, the collection did not work properly. The issue is now fixed and the events can be accessed normally in the [Event Viewer](#internal/get-to-know-insights/event-viewer).
* Fixed an issue with ULS log collection if the ULS log path was not set to default.
* Fixed a bug which caused the Alerts form to behave in an unexpected manner.
* Numerous smaller improvements and UI tweaks.





