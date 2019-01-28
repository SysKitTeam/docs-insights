---
title: SysKit Alerts
description: The SysKit Insights Alerts page gives you an overview of your alerts.
author: Tomislav Sirovec
date: 19/02/2018
---

# Alerts Dashboard

 There are five categories:

## Performance Counters

Performance Counters tab will automatically populate as soon as the application concludes the status's of the performance counters. That usually happens within 15 minutes of starting the application. The columns we provide here are: Farm, Server, Counter, Instance, Avg. Value, Time. A **red** square in front of the server name indicates that the counter is in **Critical** state. **Yellow** square indicates a **warning** status.  
Clicking on any Performance Alert will open a detailed view on the right hand side of the window. There you can find more information about the specific Performance Counter. Such as its description, the defined values for the thresholds, and the graph with the collected values. For more information on how to manage the alerts, [see this article.](../how-to/manage-alerts.md)

## Events

Events tab will be populated as soon as you define a **new Alert**. For more information on how to do this, [click here.](../how-to/manage-alerts.md)

The columns we provide here are: Farm, Server, Name, Query, Time. The square in the Server column is always grey and is indicative of Events Alert. Clicking on a Events Alert will open the details on the right hand side, which will show you the results of the defined query. Clicking on the **View Details** will preselect the query and take you to the Event Viewer screen.

## SharePoint Status

SharePoint Status tab will automatically be populated. By default SysKit Insights checks the SharePoint Timer Service status and the Central Administration \(CA\) site status. If the Timer Service job is stopped or the CA is unavailable, you will be notified every 30 minutes.  
The columns we provide here are: Farm, Server, Source, Value, Time. See the [Manage Alerts](../how-to/manage-alerts.md) article to see how you can check the status of another site.

{% hint style="warning" %}
**Please note!**   
To check \(ping\) a SharePoint site we are using the credentials of the service account you provided during the configuration of the SysKit Insights. Also, it is not possible to use forms authentication.
{% endhint %}



## Latency

The [Latency tab](latency-screen.md) will automatically populate as soon as the application finishes the first ping interval. That usually happens within 15 minutes of starting the application. The columns provided here are: Farm, Server, Bad Pings \(number of\), and Time. Click on the desired line to open the latency intervals details on the right side of the screen. This shows the **maximum latency** in that interval, number of pings sent and received, and number of pings that took longer than 1 ms.

## Page Performance

The Page Performance tab will only populate if you have added SharePoint pages to monitor. X-SPHealthScore and Page Response Time headers are monitored by default. For more information about Page Performance, [click here.](page-performance-screen.md)

## Sending the notification

In order to receive the email notification of your alerts you need to enable them. Go to Settings -&gt; Email settings. Select the: "Send email notifications when alerts occur" and fill out all the required fields.

> For more information on Insights features [see this article.](https://www.syskit.com/products/insights/features/intelligent-alerting/)

