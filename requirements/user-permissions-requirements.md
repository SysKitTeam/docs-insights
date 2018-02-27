---
title: User Permission Requirements
description: This article discusses the user permission requirements that are necessary in order to successfully use SysKit Insights.
author: Tomislav Sirovec
date: 17/01/2018
---

To run SysKit Insights and to retrieve all the data (event logs and performance counters) you want to document, SysKit Insights service account needs to have proper privileges. Here is the list of required privileges:

* __Local administrator__ on all the machines you want to monitor. Both SharePoint and SQL server.
* Minimum of __db_datareader__ on a SharePoint's Config database.
* On a SQL server - __public__ server role.

SysKit Insights relies on Active Directory to reach the names/addresses of the computer. So, the Service Account needs to have permission to __read from AD.__  
After that it uses WMI to collect all the data. Classic WMI TCP/UDP ports are used.