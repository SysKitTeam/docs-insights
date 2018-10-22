---
title: User Permission Requirements
description: This article discusses the user permission requirements that are necessary in order to successfully use SysKit Insights.
author: Tomislav Sirovec
date: 17/01/2018
---

To run SysKit Insights and to retrieve all the data (event logs and performance counters) you want to document, SysKit Insights service account needs to have proper privileges. Here is the list of required privileges:

* __Local administrator__ on all the machines you want to monitor. Both SharePoint and SQL server.
    * We are using Remote WMI to access performance metrics on SQL servers. As per [this Microsoft article](https://docs.microsoft.com/en-us/windows/desktop/wmisdk/connecting-to-wmi-on-a-remote-computer) local administrator privileges on a remote server are required to successfully access the performance data using Remote WMI approach. 
    * SysKit Insights requires local administrator privileges to access logs (ULS, Windows Event Log, SQL Log) on remote machines as well. It is not possible to access those locations remotely without local administrators privileges (Windows constraint).
* Minimum of __db_datareader__ on a SharePoint's Config database.
* On a SQL server - __public__ server role.
* The account running the SysKit Insights Configuration Wizard must have __dbcreator__ role on the SQL Server where the SysKit Insights database will be created.

SysKit Insights relies on Active Directory to reach the names/addresses of the computer. So, the Service Account needs to have permission to __read from AD.__  

After that it uses __WMI__ to collect all the data.  
__If you have a firewall between the machine hosting the application and the servers that are being monitored, you will need the following info__.

The firewall inbound rules on Windows Server 2008, 2008 R2, 2012, 2012 R2, 2016 and 2019 are (this is inside the windows firewall):

* File and printer sharing (NB-Session-In)
* Network Discovery (NB-Name-In)
* Network Discovery (NB-Datagram-In)
* COM+ Remote Administration (DCOM-In)

In case you have the third party firewall the ports are:

* RPC TCP 135
* NetBIOS Datagram Service UDP 138
* NetBIOS Name Resolution UDP 137
* NetBIOS Session Service TCP 139

Only for performance counters:

* TCP Any, the special rule in Windows Firewall [performance logs and alerts (DCOM-IN)]
* RPC TCP 135 [performance logs and alerts (TCP-IN)]
