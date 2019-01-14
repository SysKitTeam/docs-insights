---
title: SQL Cluster Issues
description: SysKit Insights cannot properly detect sql server nodes.
author: Tomislav Sirovec
date: 28/06/2018
---

# SQL Cluster Issues

The problem appears when working with servers that are a member of a Failover Cluster or Always On Availability Group.

**Summary:**  
When SysKit Insights connects to a **listener** or an **alias** that points to a Failover Cluster or Always On Availability Group the application cannot properly detect the sql server nodes.

Luckily, there is a workaround.

**Solution:**  
The problem is that, currently, application cannot automatically detect all servers \(nodes\) that are part of that Cluster.

The SysKit Insights application needs the Fully Qualified Domain Name \(FQDN\) of each server \(node\) in order to work properly. So, you need to do the following:

1. Navigate to the **Farms tab**, find the problematic Farm and click **Manage**.
2. Click the button **Add Server** and enter the servers Name and Role \(Database\).

   ![Adding more servers](https://github.com/SysKitTeam/docs-insights/tree/e279e7cb077284447b4d0daa2f424e96e445e262/known-issues/#img/addingServersToFarm_small.jpg)

3. When done adding the nodes click Save, and Save again on the Farms screen. 

**This problem affects SQL log and Performance Counters collection, as well as Latency checks.**

Make sure to give the application enough time to initialize as it can take 10-20 minutes depending on your infrastructure.

If you require more assistance with this issue, don't hesitate to [ask us.](https://www.syskit.com/company/contact-us/)

