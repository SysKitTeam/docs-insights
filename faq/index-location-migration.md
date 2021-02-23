---
description: Article will explain how to change the index location.
---

# Index Location Migration

## Change the index location to a different server or **migrate the SPDocKit Insights Agent**

If you wish to transfer the **SysKit Insights** application \(the agent that does the collection\) AND at the same time **keep the existing data** here is what you need to do:

1. **Stop** the SysKit Insights Agent service and the SysKit Insights Maintenance service.
2. Install the SysKit Insights on a different server.
3. Copy the entire index from the old to the new location.
4. Start the Configuration Wizard and: 
   1. Connect to the "old", already used Syskit Insights database 
   2. Connect to the new index location.
5. Finish the Configuration Wizard, start the application and that's it.

## Change the index location on the same server

1. **Stop** the SysKit Insights Agent service and the SysKit Insights Maintenance service.
2. Copy the entire index from the old to the new location.
3. Start the Configuration Wizard and:
   1. Connect to the "old", already used Syskit Insights database
   2. Connect to the new index location.
4. Finish the Configuration Wizard, start the application and that's it.

