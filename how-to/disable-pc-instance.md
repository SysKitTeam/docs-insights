# Disable the PC instance you do not wish to track

In case there is an instance or an entire hard drive you do not wish to track, here is how you can **disable them.**

## Disable the entire hard drive:

To disable the entire hard drive, run the following scrip against the Syskit Insights database. Set the value of variable **Enabled** to 1 or 0 \(0 = Disabled, 1 = Enabled\).  
Also, input the Server and Disk name **as they are seen in the application**.

```sql
UPDATE 
    Discs_Table 
SET 
    Enabled = 0 /* 0 = Disable, 1 = Enable */
FROM 
    [dbo].[Discs] as Discs_Table
    JOIN [EventCollection].[MonitoringServers] as Servers_Table ON Servers_Table.ID = Discs_Table.TerminalServerID
WHERE
    Servers_Table.Name = 'Insert server name here' /* Server name */
    AND Discs_Table.Name = 'Insert disk drive name' /* Disk name */
```

## Disable a specific instance:

If there is an instance, for example - hard drive instance, that you do not wish to track, here is what you need to do in order to disable it.  
Run the following scrip against the Syskit Insights database.

Set the value to the variable **Enabled** to 1 or 0 \(0 = Disabled, 1 = Enabled\).  
Also, input the Server, Counter and Instance name **as they are seen in the application**.

```sql
UPDATE 
    ServerInstance_Table 
SET 
    Enabled = 0 /* 0 = Disable, 1 = Enable */
FROM 
    [PerformanceCounters].[ServerInstances] as ServerInstance_Table
    JOIN [EventCollection].[MonitoringServers] as Servers_Table ON Servers_Table.ID = ServerInstance_Table.TerminalServerID
    JOIN [PerformanceCounters].[Counters] as Counters_Table ON Counters_Table.CounterID = ServerInstance_Table.CounterID
    JOIN [PerformanceCounters].[Instances] as Instances_Table ON Instances_Table.InstanceID = ServerInstance_Table.InstanceID
WHERE 
    Servers_Table.Name = 'Put Server name here' /* Server name */
    AND Counters_Table.DisplayName = 'Put Counter name here'  /* Counter name */
    AND Instances_Table.Name = 'Put Instance name here' /* Instance name */
```

If you require more assistance with this issue, don't hesitate to [ask us.](https://www.syskit.com/company/contact-us/)

