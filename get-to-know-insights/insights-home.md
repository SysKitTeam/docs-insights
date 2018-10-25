---
title: SysKit Insights Home 
description: The SysKit Insights home page gives you an overview of your index's contents as well as a general performance overview regarding your farm health.
author: Tomislav Sirovec
date: 25/10/2018
---

The SysKit Insights home page gives you an overview of your index's contents as well as a general performance overview regarding your farm health.
If you are monitoring multiple SharePoint farms, the farm select option will be available. Metrics shown here will change depending on the selected farm.

## Farm dashboard

If you are monitoring multiple SharePoint farms, the farm select option will be available. Metrics shown here will change depending on the selected farm.  

* __Server Status tile__ - information about how many servers are in critical, warning, healthy or offline state. 

* __Logs__ - a total number of collected events per day. If you click on the date or on the column representing the events, the graph will change into a __Logs by Server__ view and you will see total number of events __per server__ collected for the selected day.  
On top of the graph you can find __total Index size__ and __number of events__ in the index. Also, you can see index's __last update time__.  
The index size can fluctuate because of how index reorganization works. Also, since the data retention job deletes data day by day, sudden drops in this metric are possible.  

* __Alerts__ - an over of received alerts. For detailed view click the __View All Alerts__ button at the bottom of the tile. 

* __CPU utilization__ - top 3 servers with highest processor usage based on the last 15 minutes of data collected.

* __Disk Space Usage__ - top 3 disks by disk space used across all servers, based on the last collected value.

* __SharePoint Services Status__ - information whether SharePoint Timer and Search services are running on the selected farm.

* __Intra-farm Latency__ - information about which server (if any) has high latency. At the bottom, __+ X Critical Servers__ button will take you to the Latency tab and show you detailed information about latency.

* __Page Response__ - this tile will show you information about pages you are monitoring. Precisely, whether some of them has a critical status. 


## Server dashboard

To see the server dashboard, in the navigation, click on any server.

* __Logs__ - logs graph will show you the number of events __by type__, per selected server on a given day. You can see a total number of Event Log, SQL and ULS events.  

* __Alerts__ - latest alerts for the selected server. 

* __Server Performance__ - a list of performance counters currently in critical or a warning state. 

* __Services status__ - information whether there is a stopped service on the selected server.

* __Intra-farm Latency__ - information about latency status, for the selected server.


