---
title: SysKit Insights Getting Started
description: Described some of the common use cases when starting the application for the first time. 
author: Tomislav Sirovec
date: 01/03/2018
--- 
In this article we will take you through some of the common use cases and usual steps when using the application for the first time.  

- After successfully [activating](#internal/activation/online-offline-activation) the application, or starting the trial, you will be welcomed by the Farms screen. 

- First thing you need to do is [add farm/s.](#internal/get-to-know-insights/farms-screen) Until you do so, some parts of the application will be disabled. After that on the same Farms tab, you can see on overview of farms and servers you added. 

- In order to fully utilize SysKit Insights' features you need to enable the email notifications. Also, while on the settings page, note the Farms and Agents sections bellow the General Email Settings. You can navigate to the Farms section and tweak the Collection Configuration to best suit your needs. If you wish to change data collection interval, data retention or index size go to Agents section. For detailed information on settings customization see [this article.](#internal/how-to/customize-settings)

- The moment you added a new farm the data collection started. But, it will take a couple of minutes for the servers to initialize and the application to start displaying data. This usually takes a few minutes. In the mean time you can check our predefined performance counters thresholds. Navigate to the Alerts page and click [Manage Alerts.](#internal/how-to/manage-alerts) You can change them to best suits your needs, Also you can disable them completely and you will not be notified on that particular counter.    
While on the Manage Alerts form, notice the Events and SharePoint Status tabs. If you wish to be notified when something on your farm goes wrong create a new Events Alert. Also, if you are interested to know when a particular SharePoint site goes down, enable the feature in the SharePoint status tab. Notice that checking the status of the SharePoint Timer Service and the Central Administration are enabled by default. 

After all that is done you can start observing the collected data.  

## Home 
- The SysKit Insights home page gives you an overview of your index's contents as well as a general performance overview regarding your farm health.   
Event Viewer index metrics are shown per farm. If you are monitoring multiple SharePoint farms, the farm select option will be available. Metrics shown here will change depending on the selected farm.  
On the right hand side you can see a quick glance at the overall server health. For more details, please use the [performance tab.](#internal/get-to-know-insights/performance-screen) 

![Home Dashboard](#img/home-dashboard.png)

## Event Viewer
To start using the Event Viewer first select a farm. If you only have one - an automatic search will be triggered. For more details on how to use the Event Viewer, [click here.](#internal/get-to-know-insights/event-viewer)

![Event Viewer](#img/event-viewer.png)

## Performance

![Performance Screen3](#img/performance-dashboard.png) ![Performance Screen4](#img/performance-counter.png)  

![Performance Screen1](#img/performance-screen1.png) ![Performance Screen2](#img/performance-screen2.png)

