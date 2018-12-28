---
title: Manage Alerts
description: This section describes how to manage SysKit Insights Alerts.
author: Tomislav Sirovec
date: 31/1/2018
---

# manage-alerts

## Performance Counters

Here you can **manage the thresholds** and the notification settings of every performance counter. They are divided into six categories or templates: General, IIS/ASP.NET, SQL, Disk, .NET and Search.

* **Raise alert** for this counter - enable this if you wish to receive an alert when the counter reaches warning or critical threshold. Also, if any counter is either in critical or warning state, the entire server on **Performance tab** will bi marked accordingly.
* **Thresholds** - most of the counters have a predefined value. However, these values are not "one size fits all" so you can change them to suit your needs.
  * Enabling the Threshold checkboxes means that you will be alerted \(Alerts tab in the application\) when a given counter reaches its critical or warning limit. 
* Send to **default email** address will send a notification \(email\) to addresses given in Settings -&gt; Email Settings.
* Send to **alternate email** address - here you can define extra emails of people that you wish to receive the notification. 

## Events

Opening the Events tab of Manage Alerts form will show you a list of all current Alerts as well as the time the alert was last sent on. To create a new alert click **New Alert:** 1. Enter the alert name. 1. Enter your search query choose if you wish to query only the ULS logs, Event or SQL logs. Naturally you can also search for every given type of log. 1. Filter by the farm and choose how often you wish to be notified.  
1. If you wish to be notified about the alert via email check the **Send to default email address** checkbox. Also, you can send additional emails with selecting **Send to alternate email address**.

If you want to edit an already existing alert navigate to aforementioned list of alerts and on the right hand side click the edit icon for a given alert.

## SharePoint Status

### Site collection alerts

#### Following site collections are unavailable

* Check this for SysKit Insights to periodically check if the given site is online. SysKit Insights will try to access the site using the Service Account credentials.
* This can be done with any additional Windows service — please [contact us.](https://www.syskit.com/company/contact-us/) By default, this is not possible in SysKit Insights v1, but we can show you a trick ;\).

#### Central Administration status is changed

* We will continuously ping the Central Administration site and notify you if it is not accessible. By default, you will receive an alert every 30 minutes.

### Services alerts

#### SharePoint Timer Service is stopped

* Status of the SharePoint Timer Service is checked for every server in the farm. You will be alerted if the status is stopped or stopping. By default you will receive an alert every 30 minutes. 

#### SharePoint Search Service is stopped

* The status of the SharePoint Timer Service is checked for every server in the farm. You will be alerted if the status is stopped or stopping. By default, you will receive an alert every 30 minutes.

#### SharePoint User Profile service is stopped/not detected

* You will be alerted if the status is stopped or stopping. By default, you will receive an alert every 30 minutes. **Note:** The service is not available on SharePoint Server 2016.

### Intra-farm Latency

* You will be notified when the observed latency exceeds [configured](manage-alerts.md#internal/how-to/customize-settings) values. 

### Notifications

* Send to **default email** address will send a notification \(email\) to addresses given in Settings -&gt; Email Settings.
* Send to **alternate email** address - here you can define extra emails of people that you wish to receive the notification.

