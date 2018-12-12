--- 
title: SysKit Health Overview
description: The SysKit Insights Health Overview gives you an overview on the health of your farms
author: Lucija Sopic
date: 12/12/2018
---

The SysKit Insights Health Overview gives you an overview on the health of your farms which is based on the colleceted data for a selected farm and a time interval. Overview can be generated in two time intervals - from yesterday or last 7 days. It shows trend comparisons from the current interval and previously finished time interval (in percentages). Report is divided in sections:


## Events
Events section shows you the overview of events and collected logs within the selected time interval. It has two categories:
- Index size - Total disk size taken by SysKit Insights and how much it has grown since the beginnig of the interval. Its' growth depends upon farm size. Reaching maximum limit will stop Insights from collecting data.
- Entries - Overview of entries from the interval. Entries are sorted by level (Critical, Unexpected, Warning, Error and Exception) and by type (ULS, SQL and Event Log).


>For more details on Events, please [see this article.](#internal/get-to-know-insights/event-viewer)


## Performance
Performance section shows the performance overview for the farm in the selected time interval. It is divided in three categories:
- Incidents - Number of performance incidents that happened in an interval.
- By Category - Counters that have generated the greatest amount of alerts in an interval.
- By Server - Servers that have generated the greatest amount of alerts in an interval.


>For detailed information on the entire Performance section [see this article.](#internal/get-to-know-insights/performance-screen)


## Alerts
Alerts section shows the amount of alerts generated in the time interval and which types of alerts were occuring most frequently during the interval.


>For detailed information on Alerts [see this article.](#internal/get-to-know-insights/insights-alerts)


## SharePoint Services
SharePoint Services section shows the overview of SharePoint services - it gives you an insight on how many services were stopped and also how many alerts were generated for the Central Administration or services alerts in the interval.


>For detailed information on managing your Alerts [see this article.](#internal/how-to/manage-alerts)


## Page Performance
Page Performance section shows the performance overview in the time interval of SharePoint pages if you monitor any. It shows the amount of alerts that were generated for headers and file requests that you have previously enabled for monitoring.


>For detailed information on Page Performance, see [this article.](#internal/get-to-know-insights/page-performance-screen)


## Latency 
Latency section shows the latency statistics for average ping time between the servers of your farm in the selected interval. It shows if there was high latency on servers. Microsoft's standards recommed that pings should take less than 1ms to avoid bad user experience. Pings are collected every 10 minutes.


>For detailed information about Latency, see [this article.](#internal/get-to-know-insights/latency-screen)



### Schedule
If you wish, you can schedule a health report. To schedule a health report, click on the Schedule button and enable Report Scheduling. After that you can choose which sections you want to include in the report, report frequency and send time. Email settings must be configured in order to receive the report.

