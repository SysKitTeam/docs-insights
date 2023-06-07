---
description: This article describes what’s new and improved in the latest version of Syskit Insights.
---

# Syskit Insights 1.1.0

Syskit Insights 1.1.0 delivers a fresh set of new features created to make your monitoring tasks a lot easier. Keep on scrolling and see what's new!

Give it a try and let us know what you think!

**Product version:** 1.1.0  
**Build number:** 484  
**Release date:** Aug 2, 2018

[Click here to download the new release.](https://www.syskit.com/products/insights/download/)

## Features

* **Intra-farm latency**! We now check intra-farm latency. In 10-minute intervals, we ping every server in the farm. According to [Microsoft’s hardware requirements](https://docs.microsoft.com/en-us/sharepoint/install/hardware-and-software-requirements), 99.9% of pings must be under 1 ms. If they’re not, we will notify you. For detailed information about this feature, check out our [help article.](../get-to-know-insights/latency-screen.md)
* We heard your requests, and now the entire Syskit Insights application is accessible via browser as a **web application**, making it easier than ever to share reports and event log searches with your colleagues. For more information, [click here.](../get-to-know-insights/web-application.md)
* Event Viewer export: Previously, you could only export 1,000 events to Excel. You can now **specify the number of exportable events**.

## Improvements

* In the performance counters screen, it is now possible to **disable the instance \(hard drive\) you do not wish to track**. Furthermore, some hard drives \(such as Witness drives\) are hidden by default.
* Alongside SharePoint Timer Service, you can now also track **SharePoint Search Service** and **SharePoint User Profile Service**. If any of these services is stopped, we will notify you.
* We’ve added **Syskit Insights Maintenance service**. Now, the Agent and the newly added Maintenance Service will start each other if one of them fails or is unexpectedly stopped.
* In the Manage Alerts form – Performance Counters section, you will now immediately see a **green dot** if **alerting** for the corresponding counter is enabled.
* It is now possible to check the status of more than just one SharePoint site. Also, the site check URL must begin with htttp:// or https://. 
* We’ve added alerts and latency sections to the Home Dashboard. 

## Bug Fixes

* Forwarded events had a delay in collection; thus, the collection did not work properly. The issue is now fixed and the events can be accessed normally in the [Event Viewer.](../get-to-know-insights/event-viewer.md)
* Fixed an issue with ULS log collection if the ULS log path was not set to default.
* Fixed a bug which caused the Alerts form to behave in an unexpected manner.
* Numerous smaller improvements and UI tweaks.

