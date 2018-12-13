---
title: SysKit Insights Home 
description: The SysKit Insights home page gives you an overview of your index's contents as well as a general performance overview regarding your farm health.
author: Tomislav Sirovec
date: 25/10/2018
---

The SysKit Insights home page gives you an overview of a general performance regarding the health of your farms and servers, as well as events, alerts, service status or latency. If you are monitoring multiple SharePoint farms, they will all appear here. The metrics shown will change depending on which farm or server is selected.


## Farm dashboard

* __Server Status__ – Information about how many servers are in the critical, warning, healthy or offline state.
* __Logs__ – Total number of events collected per day. If you click on the date or on the column representing the events, the graph will change into a Logs by Server view and you will see the total number of events per server collected for the selected day.
The Total Index Size and Number of Events in the index are shown at the top of the graph. Also, you can see the Last Update Time of the index.
The index size can fluctuate because of how index reorganization works. Also, since the data retention job deletes data day by day, sudden drops in this metric are possible.
* __Alerts__ – An overview of alerts received for the entire farm. For a detailed view, click the View All Alerts button at the bottom of the tile.
* __CPU Utilization__ – The top three servers with the highest processor usage based on the last 15 minutes of data collected.
* __Disk Space Usage__ – The top three disks by disk space used across all servers, based on the last collected value.
* __SharePoint Services Status__ – Whether SharePoint Timer, Search, or User Profile Services are running on the selected farm.
* __Intra-farm Latency__ – Shows the servers (if any) with high latency. At the bottom, the + X Critical Servers button will take you to the latency tab, which has detailed information about latency.
* __Page Response__ – Shows whether the pages you are monitoring are offline or critical.

## Server dashboard

To see the server dashboard, click on any server in the navigation.

* __Logs__ – The graph will show the number of events by type per selected server on a given day. You can see the total number of event log, SQL and ULS events.
* __Alerts__ – The latest alerts for the selected server.
* __Server Performance__ – A list of performance counters currently in a critical or warning state.
* __Services Status__ – Whether there is a stopped service on the selected server.
* __Intra-farm Latency__ – Latency status for the selected server.


![Home Dashboard](#img/home-dashboard.png)

