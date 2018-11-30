---
title: SysKit Insights Getting Started
description: Described some of the common use cases when starting the application for the first time. 
author: Tomislav Sirovec
date: 01/03/2018
--- 
In this article we will take you through some of the common use cases and usual steps when using the application for the first time. We have provided you with an overview of the entire application and how to use it. For detailed information on certain feature please explore other articles.   

## Let's get started

After successfully [activating](#internal/activation/online-offline-activation) the application, or starting the trial, you will be welcomed by the Farms screen. 

First thing you need to do is [add farm/s.](#internal/get-to-know-insights/farms-screen) Until you do so, some parts of the application will be disabled. Afterwards, on the same Farms tab, you can see on overview of farms and servers you added. 

__Settings__

In order to fully utilize SysKit Insights' features you need to enable the email notifications. Also, while on the settings page, note the Farms and Agents sections bellow the General Email Settings. You can navigate to the Farms section and tweak the Collection Configuration to best suit your needs. If you wish to change data collection interval, data retention or index size go to Agents section.  
>For detailed information on settings customization see [this article.](#internal/how-to/customize-settings)

__Alerts__

The moment you added a new farm the data collection started. But, it will take a couple of minutes for the servers to initialize and the application to start displaying data. This usually takes a few minutes. In the meantime you can check our predefined performance counters thresholds. Navigate to the Alerts page and click [Manage Alerts.](#internal/how-to/manage-alerts) You can change them to best suits your needs, Also you can disable them completely and you will not be notified on that particular counter.    
While on the Manage Alerts form, notice the Events, SharePoint Status and Page Performance tabs. If you wish to be notified when something on your farm goes wrong create a new Events Alert. If you are interested to know when a particular SharePoint site goes down, enable the feature in the SharePoint status tab. Notice that checking the status of the SharePoint Timer Service and the Central Administration are enabled by default. Also, you can monitor the Page Performance of your SharePoint sites, such as their Page Response Time.

After all that is done you can start observing the collected data. 

## Home
- The SysKit Insights home page gives you an overview of your index's contents as well as a general performance overview regarding your farm health. If you have multiple farms you will be able to select a farm from which you want to see the general performance. You can also see the general performance of each server within the chosen farm.
On the right, when the farm is selected, Server Status and Event Viewer index metrics are shown. Metrics shown here will change depending on the selected farm. Underneath you can see the Alerts, which shows you the latest alerts on the servers within the farm.
On the right hand side you can see a quick glance of the overall server health. Next to the alerts you can also see CPU Utilization of the top 3 servers, Disk Space usage of the top 3 disks, SharePoint Services Status and Page Response. 

![Home Dashboard](#img/home-dashboard.png)

>For more details, please use the [performance tab.](#internal/get-to-know-insights/performance-screen) 

## Event Viewer
Event Viewer tab provides you with a centralized place to search for ULS, Windows Event and SQL events all over your farm. SysKit Insights uses a layout similar to a search engine to display the results, and it just that - a powerful search engine. 

To start using the Event Viewer first select a farm. If you only have one - an automatic search will be triggered. 

You can refine your query by:
- Type of event (ULS, Event Log, SQL)
    - Additional refiners such as Server and Level are positioned to the left and will modify the query text.
- Clicking on terms in the search results will also modify the query text.
    - for the compact grid layout expand the search result for this functionality to be available.  
      
When satisfied with the constructed query, press the search button again.

You have created a very useful query and would like to be notified when an event that satisfied this query appears? No problem, just create an alert by clicking the alert button on the search results page. Click [here](#internal/how-to/manage-alerts) for more details.
You can also export your logs to an Excel file.
Also, we provided more detailed information on writing the search query. See [this article.](#internal/how-to/search-query)


![Event Viewer](#img/event-viewer.png)

>For more details on how to use the Event Viewer, [click here.](#internal/get-to-know-insights/event-viewer)


## Performance

The SysKit Insights Agent relies on performance counters to monitor the server performance. The SysKit Insights calculates the following server status: Healthy, Warning, Critical, Offline or not accessible. 

The individual metrics are calculated based on their average value during the last 15 minutes. By using this approach the SysKit Insights can ignore short spikes in activity.  
The farms performance overview dashboard shows all farms currently monitored by SysKit Insights Agent. It shows status for each server in those farms. 

__Detailed Farm Overview Dashboard__

The detailed farm overview dashboard shows more in-depth data about each server in the farm but is limited to just a single farm. 

__Server Overview Dashboard__

The server overview dashboard shows all metrics that are collected for each server. The metrics are separated in different categories. The server role in the SharePoint farm determines which categories are assigned to each server.  

![Performance Dashboard](#img/performance-dashboard.png) ![Performance Screen2](#img/performance-screen2.png)  

>For detailed information on the entire Performance section [see this article.](#internal/get-to-know-insights/performance-screen)

## Alerts

The SysKit Insights Alerts page gives you an overview of your alerts. There are five categories: Performance Counters, Events, SharePoint Status, Latency and Page Performance.

In order to receive the email notification of your alerts you need to enable them. Go to Settings -> Email settings. Select the: "Send email notifications when alerts occur" and fill out all the required fields.

![Manage Alerts](#img/manage-alerts.png) ![Event Alert](#img/event-alert.png)  

>For detailed information on managing your Alerts [see this article.](#internal/how-to/manage-alerts)

## Latency

The SysKit Insights latency screen gives you a detailed overview of all the ping intervals made. Latency indicates the delay in the communication between the servers and is important as a hardware requirement. High latency is usually indicator of a bigger underlying problem, and should be inspected. 


In [this article](#internal/get-to-know-insights/latency-screen) we provide a detailed information about the Latency tab.  

## Page Performance 

SysKit Insights monitors the performance of SharePoint pages by periodically collecting page performance data. Here you can add and manage pages that you wish to monitor. You can monitor both SharePoint On-Premises and SharePoint Online sites/pages. Pages are pinged constantly throughout the day. Various parameters can be monitored - such as the availability of the page, page response time, SharePoint specific header metrics, or simply - you can observe if there is a huge picture of someone's cat slowing down the page opening time. 

![Page Performance Dashboard](#img/page-performance.png)

In [this article](#internal/get-to-know-insights/page-performance-screen) we provide a detailed information about the Page Performance tab.

## Farms

On the main application window click __Farms.__ You will see a number of added farms, servers and a License Server Limit, as well as an overview of all the servers in farms.  

In [this article](#internal/get-to-know-insights/farms-screen) we provides detailed overview of farms and servers that are being tracked. Also, it explains different options on how to add a new farm or a new server into an existing farm.


