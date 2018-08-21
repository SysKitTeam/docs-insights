---
title: SysKit Insights Agent migration FAQ
description: Article will explain how to change the index location.
author: Tomislav Sirovec
date: 21/08/2018
---

This article will explain how to change the index location.

## Change the index location to a different server or __migrate the Agent from SPDocKit Insights__
If you wish to transfer the __SysKit Insights__ application (the agent that does the collection) AND at the same time __keep the existing data__ here is what you need to do:  
1. __Stop__ the SysKit Insights Agent service and the SysKit Insights Maintenance service.
1. Install the SysKit Insights on a different server.
1. Copy the entire index from the old to the new location.
1. Start the Configuration Wizard and:
    1. Connect to the "old", already used Syskit Insights database
    2. Connect to the new index location.
1. Finish the Configuration Wizard, start the application and that's it.



## Change the index location on the same server
1. __Stop__ the SysKit Insights Agent service and the SysKit Insights Maintenance service.
1. Copy the entire index from the old to the new location.
1. Start the Configuration Wizard and:
    1. Connect to the "old", already used Syskit Insights database
    2. Connect to the new index location.
1. Finish the Configuration Wizard, start the application and that's it.
