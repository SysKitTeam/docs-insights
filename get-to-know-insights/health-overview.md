# health-overview

title: Health Overview description: The SysKit Insights Health Overview gives you an overview on the health of your farms author: Lucija Sopic

## date: 12/12/2018

The SysKit Insights Health Overview gives you an instant overview on the health of your farms, which is based on the data gathered for a selected farm and time interval. An overview can be generated for two time intervals — “Yesterday” or “Last 7 days.” It shows trend comparisons for the current interval and for the previously completed time interval \(in percentages\). Each report is divided into the following sections:

## Events

The Events section provides an overview of events and collected logs within a selected time interval. It has two categories:

* Index size— the total disk space occupied by  SysKit Insights and how much it has grown since the start of the interval. Its growth depends upon the farm size. Insights will stop collecting data once a maximum limit has been reached.
* Entries—an overview of entries for that interval. Entries are sorted by level \(Critical, Unexpected, Warning, Error and Exception\) and by type \(ULS, SQL and Event Log\).

> For more details on Events, please [see this article.](health-overview.md#internal/get-to-know-insights/event-viewer)

## Performance

The Performance section provides a performance overview for your farm for a selected time interval. It is divided into the following three categories:

* Incidents — the number of performance incidents that have occurred in a set interval;
* By category — the counters that have generated the highest number of alerts in a set interval;
* By server — the servers that have generated the highest number of alerts in a set interval.

> For more details on performance please [see this article.](health-overview.md#internal/get-to-know-insights/performance-screen)

## Alerts

The Alerts section shows the number of alerts generated in a specified time interval and which types of alerts occurred most frequently during this interval.

> For more details on Alerts [see this article.](health-overview.md#internal/get-to-know-insights/insights-alerts)

## SharePoint Services

The SharePoint Services section provides an overview of SharePoint services, giving you an insight into how many services were stopped, and also how many alerts were generated for the Central Administration or how many service alerts were generated in a specified interval.

> For detailed information on managing your SharePoint services, please [see this article.](health-overview.md#internal/how-to/manage-alerts#sharepoint-status)

## Page Performance

The Page Performance section provides a performance overview on the time interval of any SharePoint pages you monitor. It shows the number of alerts that were generated for all headers and file requests that you have previously enabled for monitoring.

> For more details on page performance, please see [this article.](health-overview.md#internal/get-to-know-insights/page-performance-screen)

## Latency

The Latency section shows the latency statistics for average ping time between the servers of your farm for a selected interval. It highlights whether there was high latency on the servers. Microsoft recommends that pings should take less than 1 ms, to avoid bad user experience. Pings are recorded every 10 minutes.

> For more details on latency, please see [this article.](health-overview.md#internal/get-to-know-insights/latency-screen)

### Schedule

If you wish, you can schedule a health report. To do so, click on the Schedule button and enable Report Scheduling. After that you can choose which sections you want to include in the report, and opt to receive info on report frequency and send time. To receive the report, your email settings must be configured.

