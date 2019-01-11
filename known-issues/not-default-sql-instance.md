---
title: SQL server instance name is not default
description: >-
  SQL server instance name that is being used for SharePoint is not  MSSQL's
  default.
author: Tomislav Sirovec
date: 19/09/2018
---

# not-default-sql-instance

**Summary:** SQL server instance name that is being used for SharePoint is not default MSSQL's.

**Solution:** You need to change the Parameter **@InstanceName='SHAREPOINT'**;  
Here you need to **input the name of your instance**. If your instance is named SERVERNAME/JOHN then you would set the InstanceName to "JOHN".

After the script is run against the SysKit Insights database you will need to **restart the SysKit Insights Agent service.** If the problem still persists you should consider restarting the SQL server, as we have found that this helps in some cases.

**Please note!** Always keep the SysKit Insights application updated to the newest version.

```sql
declare @InstanceName varchar(200);
set @InstanceName='SHAREPOINT';

UPDATE PerformanceCounters.Categories
set ClassName = CONCAT('Win32_PerfRawData_MSSQL', @InstanceName, '_MSSQL', @InstanceName, 'GeneralStatistics')
where ClassName LIKE '%GeneralStatistics%'

UPDATE PerformanceCounters.Categories
set ClassName = CONCAT('Win32_PerfRawData_MSSQL', @InstanceName, '_MSSQL', @InstanceName, 'BufferManager')
where ClassName LIKE '%BufferManager%'

UPDATE PerformanceCounters.Categories
set ClassName = CONCAT('Win32_PerfRawData_MSSQL', @InstanceName, '_MSSQL', @InstanceName, 'SQLStatistics')
where ClassName LIKE '%SQLStatistics%'

UPDATE PerformanceCounters.Categories
set ClassName = CONCAT('Win32_PerfRawData_MSSQL', @InstanceName, '_MSSQL', @InstanceName, 'AccessMethods')
where ClassName LIKE '%AccessMethods%'

UPDATE PerformanceCounters.Categories
set ClassName =  CONCAT('Win32_PerfRawData_MSSQL', @InstanceName, '_MSSQL', @InstanceName, 'Latches')
where ClassName like '%Latches%'

UPDATE PerformanceCounters.Categories
set ClassName = CONCAT('Win32_PerfRawData_MSSQL', @InstanceName, '_MSSQL', @InstanceName, 'Locks')
where ClassName like '%Locks%'

UPDATE PerformanceCounters.Categories
set ClassName = CONCAT('Win32_PerfRawData_MSSQL', @InstanceName, '_MSSQL', @InstanceName, 'Databases')
where ClassName like '%Databases%'
```

If you require more assistance with this issue, don't hesitate to [ask us.](https://www.syskit.com/company/contact-us/)

