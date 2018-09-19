---
title: SQL Cluster Issues.
description: SysKit Insights cannot properly detect sql server nodes.
author: Tomislav Sirovec
date: 28/06/2018
---

The problem appears when working with servers that are a member of a Failover Cluster or Always On Availability Group.

__Summary:__  
When SysKit Insights connects to a __listener__ or an __alias__ that points to a Failover Cluster or Always On Availability Group the application cannot properly detect the sql server nodes.
 
Luckily, there is a workaround. 

__Solution:__  
The problem is that, currently, application cannot automatically detect all servers (nodes) that are part of that Cluster.  

The SysKit Insights application needs the Fully Qualified Domain Name (FQDN) of each server (node) in order to work properly. So, you need to do the following:

 1. Navigate to the __Farms tab__, find the problematic Farm and click __Manage__.
1. Click the button __Add Server__ and enter the servers Name and Role (Database).

   ![Adding more servers](#img/addingServersToFarm_small.jpg)


1. When done adding the nodes click Save, and Save again on the Farms screen. 

__This problem affects SQL log and Performance Counters collection, as well as Latency checks.__

Make sure to give the application enough time to initialize as it can take 10-20 minutes depending on your infrastructure.  

If you require more assistance with this issue, don't hesitate to [ask us.](https://www.syskit.com/company/contact-us/)