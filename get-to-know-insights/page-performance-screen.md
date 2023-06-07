---
description: Detailed overview on how the Syskit Insights monitors Page Performance.
---

# Page Performance Screen

First you need to:

**Add New Page** 1. On the **Page Performance tab, click Add New.**

1. Select the farm for which you wish to add pages \(if you have more than one\).
2. Enter the pages you wish to monitor, either one by one or by importing them from a file. When importing from a file, put each page on a separate line.
3. Click **Import** and the import check will start.
   * For on-premises pages, we use the service account you provided in the configuration wizard. You need to ensure that this account has the necessary permissions. 
   * If you want to monitor a **SharePoint Online site**, a popup window will ask you to provide the required credentials. When prompted to remember the login, make sure to click **yes**. The benefits are:
     * Credentials will be reused for all connections to the same tenant.
     * The credentials will be valid for more than 5 days.
     * For more about monitoring SharePoint Online sites, [click here.](../how-to/spo-pp.md)

The pages added will be shown on the Page Performance dashboard.

## Page Performance Dashboard

**The data shown here are average values**, calculated for the period selected in the data range filter, which is by default the last 24h.

If you want to receive a notification when a metric exceeds its threshold, then set up an alert. For more information on how to do so, please see [this article.](../how-to/manage-alerts.md#page-performance)

Metrics over their threshold will be red on the dashboard. If they are under their threshold, they will be green.

If you click on a page \(each entire row is clickable\), you will see detailed information about that page, such as SharePoint header metrics and file requests.

## Page Headers

* **Uptime** - Calculated time of page availability during the selected period \(based on the data range filter\).
* **X-SPHealthScore** - The server can monitor the current load and its ability to process requests. If it is monitoring the load, it will return load information to the client in the X-SPHealthScore header. This header is between 0 and 10, where 0 represents a low load and a high ability to process requests and 10 represent a high load and that the server is throttling requests to maintain adequate throughput.
* **SPRequestDuration** - This is how long, in milliseconds, a request took to process on the server.
* **SPIISLatency** - The time in milliseconds taken in the front-end web server after the request has been received by the front-end web server before the web application begins processing the request.
* **Page Response Time** - The total time in milliseconds required to download the page.
* **SPRequestGuid** - While ULS logs have correlation IDs, SharePoint pages have request GUIDs.

## File Requests

The File Requests feature simulates real-world page usage. There is no caching and the numbers shown are what a real user might expect when accessing the page. Syskit Insights will try to load and emulate the browser opening the page.

The data shown are from the 20-second interval during which Syskit Insights monitors the page.

You can monitor **Size, Load Time**, and **Item Count** for certain elements of the page. These elements are: **HTML, JavaScript, images, CSS, and Fonts**.  
Syskit Insights uses **The Coach** to monitor performance of your pages, and from the information collected, we calculate the Page Score. For more information, please see [this link](https://www.sitespeed.io/documentation/coach/introduction/).

On the right-hand side, there is a waterfall model of a page, like the one you can find in Google Chrome's DevTools, showing you every element loaded.

File requests are collected every 6 hours.

