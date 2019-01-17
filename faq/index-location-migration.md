---
title: SysKit Insights Agent migration FAQ
description: This article will explain how to change the index location.
author: Tomislav Sirovec
date: 21/08/2018
---

# Index Location Migration

## Change the index location to a different server or **migrate the SPDocKit Insights Agent**

If you wish to transfer the **SysKit Insights** application \(the agent that does the collection\) AND at the same time **keep the existing data** here is what you need to do:  
1. **Stop** the SysKit Insights Agent service and the SysKit Insights Maintenance service. 1. Install the SysKit Insights on a different server. 1. Copy the entire index from the old to the new location. 1. Start the Configuration Wizard and: 1. Connect to the "old", already used Syskit Insights database 2. Connect to the new index location. 1. Finish the Configuration Wizard, start the application and that's it.

## Change the index location on the same server

1. **Stop** the SysKit Insights Agent service and the SysKit Insights Maintenance service.
2. Copy the entire index from the old to the new location.
3. Start the Configuration Wizard and:
   1. Connect to the "old", already used Syskit Insights database
   2. Connect to the new index location.
4. Finish the Configuration Wizard, start the application and that's it.

