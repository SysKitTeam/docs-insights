---
title: SQL logs are not being collected for servers in a SQL cluster.
description: SQL logs are not being collected for servers in a Failover Cluster or AlwaysOn Availability Group.
author: Tomislav Sirovec
date: 28/06/2018
---

__Summary:__  
The problem appears when trying to collect SQL logs from servers that are a member of a Failover Cluster or Always On Availability Group. In this case, out of the box collection of SQL logs is currently not supported.  
But, there is a workaround. 

__Solution:__  
The problem is that application cannot currently automatically detect all servers (nodes) that are part of that Cluster.  
So, you need to do the following: 
1. Navigate to the __Farms tab__, find the problematic Farm and click __Manage__.
1. Click the button __Add Server__ and enter the servers Name and Role (Database).

   ![Adding more servers](#img/addingServersToFarm.png)

1. When done adding the nodes click Save, and Save again on the Farms screen.

And that is it. Make sure to wait for logs to be collected as it can take 10-20 minutes depending on your infrastructure.  
Then, navigate to the [Event Viewer tab](#internal/get-to-know-insights/event-viewer) and search for your logs. 


If you require more assistance with this issue, don't hesitate to [ask us.](https://www.syskit.com/company/contact-us/)