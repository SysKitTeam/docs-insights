---
title: SysKit Insights 2 - Release Note
description: This article describes what’s new and improved in the latest version of SysKit Insights.
author: Tomislav Sirovec
date: 22/10/2018
---

This release is all about the __Page Performance!__ From now on, you can monitor End-User Experience and detect if your SharePoint pages are slow for your users.  
SysKit Insights now supports SharePoint on-premises, SharePoint Online, and hybrid SharePoint environments. You can easily monitor simple but essential information like page's uptime, load time, or more complex, like every loaded element of a page to find the cause of the slowdown. 

Give it a try and let us know what you think!

__Product version:__ 2.0.0  
__Build number:__ 700    
__Release date:__ Oct 30, 2018  

[Click here to download the new release.](https://www.syskit.com/products/insights/download/)

## Features

- The main new feature in this release is __Page Performance!__ It allows you to monitor SharePoint pages, and gain valuable insights into their performance.  
__Receive alerts and spot critical metrics__ for each monitored page. You can also export SharePoint page performance metrics and drill down to find trends and improve the experience for your users.  
Oh, SharePoint Online pages are also supported! :)  
  > For detailed information about this feature, please see [this article.](#internal/get-to-know-insights/page-performance-screen)

- __Full support for SharePoint 2019__

## Improvements
- The dashboard has been __redesigned and improved!__ The left-hand side gives an overview of all your farms and the servers in them, while the right-hand side shows the content, with an overview of your logs, alerts, performance counters, SharePoint service status, farm latency, and page performance.
- The SysKit Insights web application can now be started with a desktop shortcut. 
- On the alerts tab, there is now a __filter instead of tabs__, making the interface much cleaner and easier to use. 
- The SharePoint search service is now checked __only on a SP search server.__ __The user profile service is disabled by default.__
- We have improved the way we check for high latency. Now, fewer resources will be used. 
- It has come to our attention that latency alerts were being sent way too often. So, the __default period__ for latency alerts __has been increased from 30 minutes to 12 hours.__
- We have added a type column to the event log export. 
- There are numerous performance improvements. 

## Bug fixes

- Fixed a bug when using the Express license. The application was sending out email alerts when it should not have. Also, a number of smaller bug fixes concerning the Express license. 
- When you deleted a server, it was still visible on the latency tab. Now fixed. 
- Fixed an issue with detecting multiple agents during an upgrade.
- Fixed an issue when trying to use the “none” grouping of servers on the performance tab. 
- Fixed an issue with the collection of ULS logs on SharePoint 2019 farms. 

## Discontinued Features
- With the introduction of the page performance feature, the “Site Collections are unavailable” alert has become obsolete. 
- The Express license has been discontinued. Instead, you can use the free tool SysKit Insights Lite. 
