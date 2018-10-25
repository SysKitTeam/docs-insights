---
title: SysKit Insights Page Performance 
description: Detailed overview on how the SysKit Insights monitors Page Performance.
author: Tomislav Sirovec
date: 22/10/2018
---

SysKit Insights monitors the performance of SharePoint pages by periodically collecting page performance data. 

First thing you need to do is:

__Add New Page__
1. While on __Page Performance tab, click Add New__.
2. Select a farm for which you wish to add pages. 
3. Enter the pages you want to monitor, either one by one, or you can import them from a file. When importing from a file, separate the pages with a newline.
4. Click __Import__ and the import check will start. If you entered the page for which you do not have privileges - a pop up window will ask you to provide credentials that does. The same goes if you wish to monitor a __SharePoint Online site__. A popup window will ask you to provide the required credentials. When prompted to remember the login make sure to click __yes__. The benefits are:
    - Credentials will be reused for all connections to the same tenant.
    - The credentials will be valid for more than 5 days.


After adding all the pages you wish, they will be shown on the Page Performance dashboard.

## Page Performance Dashboard

__The data shown here will be average__ - which is calculated for a period selected in a Data Range filter, by default - Last 24h.  
If you wish to monitor certain metrics in order to receive alerts when said values exceed set thresholds, you need to set up the Alerts. For more information on how to do so - see [this article](#internal/how-to/manage-alerts#page-performance). When certain metric exceed the set threshold they will be colored red on the dashboard. If the metric is under the threshold it will be colored green.  

You can click on a page (entire row is clickable) and you will see detailed information about it - SharePoint Header Metrics and File Requests. 

## Page headers

* __Uptime__ - Calculated time of page availability during the selected period (in the Data range filter).

* __X-SPHealthScore__ - The server can monitor the current load and its ability to process requests. If it monitors the load, it can return the load information to the client in a X-SPHealthScore header. This header specifies a value between 0 and 10m where 0 represents a low load and a high ability to process requests and 10 represent a high load and that the server is throttling requests to maintain adequate throughput. 

* __SPRequestDuration__ - SPRequestDuration which is the value, in milliseconds, of how long a request took to process on the server. 

* __SPIISLatency__ - SPIISLatency is the time in milliseconds taken in the front-end Web Server after the request has been received from the front-end Web server, but before the Web Application begins processing the request. 

* __Page Response Time__ - Total time in milliseconds required to download the page.

* __SPRequestGuid__ - While ULS logs have Correlation IDs, SharePoint pages have request guids.


## File Requests

File Requests feature simulates real world page usage. There is no caching and the numbers here are what a real user might expect when accessing the page. 

You can monitor __Size, Load Time__, and __Item Count__ for certain elements of the page. These elements are: __HTML, Javascript, Images, SCC, Fonts__.  
SysKit Insights uses __The Coach__ to monitor performance of your pages, and based on it, we provide you with a page's __Page Score__. For more information see [this link](https://www.sitespeed.io/documentation/coach/introduction/). 

On the right hand side there is a waterfall model of a page, like the one you can find in Google Chrome's DevTools, showing you every loaded element. 

File Request are collected every 6 hours. 