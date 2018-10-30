---
title: SysKit Insights 2.0.0 - Release Note
description: This article describes what’s new and improved in the latest version of SysKit Insights.
author: Tomislav Sirovec
date: 22/10/2018
---

This release is all about the __Page Performance!__ From now on, you can monitor End-User Experience and proactively track if your SharePoint pages are slow for your users.  
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
- The SharePoint search service is now checked __only on a SP Search Server.__ __The User Profile Service is disabled by default.__
- It has come to our attention that latency alerts were being sent way too often. So, the __default period__ for latency alerts __has been increased from 30 minutes to 12 hours.__
- We have added a Event type (SQL, ULS, Event Log) column to the event log export. 
- There are numerous performance improvements. 

## Bug fixes

- Fixed an issue when the deleted server remained visible on the Latency tab
- Fixed an issue with detecting multiple agents during an upgrade.
- Fixed an issue when trying to use the “none” grouping of servers on the Performance tab. 
- Fixed an issue with the collection of ULS logs on SharePoint 2019 farms. 

## Discontinued Features
- With the introduction of the Page Performance feature, the “Site Collections are unavailable” alert has become obsolete. See [this article](#internal/get-to-know-insights/page-performance-screen) for more information on how to monitor your pages with the new Page Performance feature. 
- The Express license has been discontinued. Instead, you can use the free tool [SysKit Insights Lite.](https://www.syskit.com/products/insights-lite/download) 


Your feedback and suggestions will help us build better SharePoint admin tools, so please feel free to [contact us](https://www.syskit.com/company/contact-us/) and send us your feedback and suggestions.