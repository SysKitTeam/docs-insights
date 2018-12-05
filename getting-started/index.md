---
title: SysKit Insights Getting Started
description: Described some of the common use cases when starting the application for the first time. 
author: Tomislav Sirovec
date: 01/03/2018
--- 
In this article we will take you through some of the common use cases and usual steps when using the application for the first time. We have provided you with an overview of the entire application and how to use it. For detailed information on certain feature please explore other articles.   

## Let's get started

After successfully [activating](#internal/activation/online-offline-activation) the application, or starting the trial, you will be welcomed by the Farms screen. 
 
## Farms

- First thing you need to do is [add farm/s.](#internal/get-to-know-insights/farms-screen) Until you do so, some parts of the application will be disabled. Afterwards, on the same Farms tab, you can see on overview of farms and servers you added, as well as the License Server Limit.  

In [this article](#internal/get-to-know-insights/farms-screen) we provides detailed overview of farms and servers that are being tracked. Also, it explains different options on how to add a new farm or a new server into an existing farm.

After all that is done you can start observing the collected data. 

![Farms](#img/farms-screen.png)

## Home

The SysKit Insights home page gives you an overview of a general performance regarding the health of your farms and servers, as well as events, alerts, service status or latency - it depends on whether you have selected a farm or a server. From here, you can access any other tab.

- If you have multiple farms you will be able to select a farm from which you want to see the general performance. You can also see the general performance of each server within the chosen farm.

![Home Dashboard](#img/home-dashboard.png)

>For more details, please use the [performance tab.](#internal/get-to-know-insights/performance-screen) 

## Event Viewer

Event Viewer tab provides you with a centralized place to search for ULS, Windows Event and SQL events all over your farm. SysKit Insights uses a layout similar to a search engine to display the results, and it just that - a powerful search engine. 

- To start using the Event Viewer first select a farm. If you only have one - an automatic search will be triggered. 

- If you would like to be alerted for events that match a specific query, you can do so in Alert Me option.

- Also, we provided more detailed information on writing the search query. See [this article.](#internal/how-to/search-query)

![Event Viewer](#img/event-viewer.png)

>For more details on how to use the Event Viewer, [click here.](#internal/get-to-know-insights/event-viewer)

## Performance

The SysKit Insights Agent relies on performance counters to monitor the server performance. The SysKit Insights calculates the following server status: Healthy, Warning, Critical, Offline or not accessible. 

- The individual metrics are calculated based on their average value during the last 15 minutes. By using this approach the SysKit Insights can ignore short spikes in activity.  
- The farms performance overview dashboard shows all farms currently monitored by SysKit Insights Agent. It shows status for each server in those farms. 

![Performance Dashboard](#img/performance-dashboard.png) ![Performance Screen2](#img/performance-screen2.png)  

>For detailed information on the entire Performance section [see this article.](#internal/get-to-know-insights/performance-screen)

## Alerts

The SysKit Insights Alerts page gives you an overview of your alerts. There are five categories: Performance Counters, Events, SharePoint Status, Latency and Page Performance. Alerts are useful because you can be warned about any unwanted performance drops or if a log appeared that matches the query that you wanted to be notified about.

- When you add a new farm, will take a couple of minutes for the servers to initialize and the application to start displaying data.

- Performance counters have predefined thresholds that can be modified to best suit your needs.

![Manage Alerts](#img/manage-alerts.png) ![Event Alert](#img/event-alert.png)  

>For detailed information on managing your Alerts [see this article.](#internal/how-to/manage-alerts)

## Latency

The SysKit Insights latency screen gives you a detailed overview of all the ping intervals made. 

- Latency indicates the delay in the communication between the servers and is important as a hardware requirement. High latency is usually indicator of a bigger underlying problem, and should be inspected. 

>In [this article](#internal/get-to-know-insights/latency-screen) we provide a detailed information about the Latency tab.  

## Page Performance 

SysKit Insights monitors the performance of SharePoint pages by periodically collecting page performance data. Here you can add and manage pages that you wish to monitor. 

- You can monitor both SharePoint On-Premises and SharePoint Online sites/pages. 

- Pages are pinged constantly throughout the day. 

- Various parameters can be monitored - such as the availability of the page, page response time, SharePoint specific header metrics, or simply - you can observe if there is a huge picture of someone's cat slowing down the page opening time.

![Page Performance Dashboard](#img/page-performance.png)

>In [this article](#internal/get-to-know-insights/page-performance-screen) we provide a detailed information about the Page Performance tab.

## Settings

In order to fully utilize SysKit Insights' features you need to enable the email notifications. Also, while on the settings page, note the Farms and Agents sections bellow the General Email Settings. 

- You can navigate to the Farms section and tweak the Collection Configuration to best suit your needs. 

- If you wish to change data collection interval, data retention or index size go to Agents section.  

>For detailed information on settings customization see [this article.](#internal/how-to/customize-settings)


