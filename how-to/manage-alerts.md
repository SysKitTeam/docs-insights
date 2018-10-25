---
title: Manage Alerts
description: This section describes how to manage SysKit Insights Alerts.
author: Tomislav Sirovec
date: 31/1/2018
---

# Performance Counters

Here you can __manage the thresholds__ and the notification settings of every performance counter. They are divided into six categories or templates: General, IIS/ASP.NET, SQL, Disk, .NET and Search.
- __Raise alert__ for this counter - enable this if you wish to receive an alert when the counter reaches warning or critical threshold. Also, if any counter is either in critical or warning state, the entire server on __Performance tab__ will bi marked accordingly.
- __Thresholds__ - most of the counters have a predefined value. However, these values are not "one size fits all" so you can change them to suit your needs.
    - Enabling the Threshold checkboxes means that you will be alerted (Alerts tab in the application) when a given counter reaches its critical or warning limit. 

- Send to __default email__ address will send a notification (email) to addresses given in Settings -> Email Settings.
- Send to __alternate email__ address - here you can define extra emails of people that you wish to receive the notification. 

# Events

Opening the Events tab of Manage Alerts form will show you a list of all current Alerts as well as the time the alert was last sent on. 
To create a new alert click __New Alert:__
1. Enter the alert name.
1. Enter your search query choose if you wish to query only the ULS logs, Event or SQL logs. Naturally you can also search for every given type of log.
1. Filter by the farm and choose how often you wish to be notified.  
1. If you wish to be notified about the alert via email check the __Send to default email address__ checkbox. Also, you can send additional emails with selecting __Send to alternate email address__.  

If you want to edit an already existing alert navigate to aforementioned list of alerts and on the right hand side click the edit icon for a given alert. 

# SharePoint Status

## Site collection alerts
### Following site collections are unavailable
* Check this for SysKit Insights to periodically check if the given site is online. SysKit Insights will try to access the site using the Service Account credentials.
*  This can be done with any additional Windows service — please [contact us.](https://www.syskit.com/company/contact-us/) By default, this is not possible in SysKit Insights v1, but we can show you a trick ;).

### Central Administration status is changed
* We will continuously ping the Central Administration site and notify you if it is not accessible. By default, you will receive an alert every 30 minutes.

## Services alerts
### SharePoint Timer Service is stopped
* Status of the SharePoint Timer Service is checked for every server in the farm. You will be alerted if the status is stopped or stopping. By default you will receive an alert every 30 minutes. 

### SharePoint Search Service is stopped
* The status of the SharePoint Timer Service is checked for every server in the farm. You will be alerted if the status is stopped or stopping. By default, you will receive an alert every 30 minutes.

### SharePoint User Profile service is stopped/not detected
* You will be alerted if the status is stopped or stopping. By default, you will receive an alert every 30 minutes. __Note:__ The service is not available on SharePoint Server 2016.

## Intra-farm Latency
* You will be notified when the observed latency exceeds [configured](#internal/how-to/customize-settings) values. 


## Notifications

- Send to __default email__ address will send a notification (email) to addresses given in Settings -> Email Settings.
- Send to __alternate email__ address - here you can define extra emails of people that you wish to receive the notification.

# Page Performance

Here you can configure which metric to monitor in order to send alerts if received values exceed set thresholds. 

- Enable Page Performance Alerting - check this to enable the alerting.

## General
- SPRequestDuration - by default 150ms and OFF
- SPIISLatency - by default 9ms and OFF
- X-SPHealthScore - by default 4 and __ON__
- Page Response Time - by default 5000ms and __ON__

## Javascript
- File Size - default 2000kB and OFF
- File Load Time - - default 2000ms and OFF

## CSS
- File Size - by default 2000kB and OFF
- File Load Time - by default 2000ms and OFF

## Notifications

- Send to __default email__ address will send a notification (email) to addresses given in Settings -> Email Settings.
- Send to __alternate email__ address - here you can define extra emails of people that you wish to receive the notification.