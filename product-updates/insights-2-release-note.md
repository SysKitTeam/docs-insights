---
title: SysKit Insights 2.0.0 - Release Note
description: >-
  This article describes what’s new and improved in the latest version of SysKit
  Insights.
author: Tomislav Sirovec
date: 22/10/2018
---

# insights-2-release-note

This release is all about the **Page Performance!** From now on, you can monitor End-User Experience and proactively track if your SharePoint pages are slow for your users.  
SysKit Insights now supports SharePoint on-premises, SharePoint Online, and hybrid SharePoint environments. You can easily monitor simple but essential information like page's uptime, load time, or more complex, like every loaded element of a page to find the cause of the slowdown.

Give it a try and let us know what you think!

**Product version:** 2.0.0  
**Build number:** 802  
**Release date:** Oct 30, 2018

[Click here to download the new release.](https://www.syskit.com/products/insights/download/)

## Features

* The main new feature in this release is **Page Performance!** It allows you to monitor SharePoint pages, and gain valuable insights into their performance.  
  **Receive alerts and spot critical metrics** for each monitored page. You can also export SharePoint page performance metrics and drill down to find trends and improve the experience for your users.  
  Oh, SharePoint Online pages are also supported! :\)

  > For detailed information about this feature, please see [this article.](insights-2-release-note.md#internal/get-to-know-insights/page-performance-screen)

* **Full support for SharePoint 2019**

## Improvements

* The dashboard has been **redesigned and improved!** The left-hand side gives an overview of all your farms and the servers in them, while the right-hand side shows the content, with an overview of your logs, alerts, performance counters, SharePoint service status, farm latency, and page performance.
* The SysKit Insights web application can now be started with a desktop shortcut. 
* The SharePoint search service is now checked **only on a SP Search Server.** **The User Profile Service is disabled by default.**
* It has come to our attention that latency alerts were being sent way too often. So, the **default period** for latency alerts **has been increased from 30 minutes to 12 hours.**
* We have added a Event type \(SQL, ULS, Event Log\) column to the event log export. 
* There are numerous performance improvements. 

## Bug fixes

* Fixed an issue when the deleted server remained visible on the Latency tab
* Fixed an issue with detecting multiple agents during an upgrade.
* Fixed an issue when trying to use the “none” grouping of servers on the Performance tab. 
* Fixed an issue with the collection of ULS logs on SharePoint 2019 farms. 

## Discontinued Features

* With the introduction of the Page Performance feature, the “Site Collections are unavailable” alert has become obsolete. See [this article](insights-2-release-note.md#internal/get-to-know-insights/page-performance-screen) for more information on how to monitor your pages with the new Page Performance feature. 
* The Express license has been discontinued. Instead, you can use the free tool [SysKit Insights Lite.](https://www.syskit.com/products/insights-lite/download) 

Your feedback and suggestions will help us build better SharePoint admin tools, so please feel free to [contact us](https://www.syskit.com/company/contact-us/) and send us your feedback and suggestions.

