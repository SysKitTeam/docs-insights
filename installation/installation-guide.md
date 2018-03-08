---
title: Install SysKit Insights
description: This section describes how to configure, that is install, SysKit Insights
author: Tomislav Sirovec
date: 06/02/2018
---

SysKit Insights provides continuous load of the SharePoint ULS, Windows Event logs and SQL logs in real-time. The SysKit Insights Agent will gather selected events and store them on __index location on your disk__. SysKit Insights presents a centralized place for you to explore, detect and prevent possible issues appearing on your SharePoint farm. Performance data is also collected and is stored in the __SysKit Insights database__.

Use SysKit Insights to keep multiple farms under control and find problems more easily.  

Before we get started __please note!__ We recommend installing the application on a machine outside of the SharePoint farm/s you wish to monitor. 


1. [Download](https://www.syskit.com/products/insights/) Application.
2. Unpack and run __SysKitInsightsSetup.exe.__ The wizard will guide you through the installation steps, click Next > to proceed.
3. Click I Accept the terms of the license agreement to accept the license and then click Next > to proceed.
4. Choose the installation folder e.g. __C:\Program Files\SysKit\Insights.__ Click __Next__ > to proceed.
5. Select the location where to create application shortcuts and the preferred availability option (__Anyone__ or __Only me__). Click __Next__ > to proceed.
6. The installation wizard will unpack your files and you will be able to run the application from: __Start__ > __All Programs__ > __Syskit Insights.__

And that is it. The application is installed. Now we need to setup the SysKit Agent. This is how:

After the installation is done, SysKit Insights  - Configuration Wizard will automatically start. Alternatively, you can start it manually by running it from the installation folder (default is C:\Program Files\SysKit\Insights\Service\SysKit.Insights.ConfigurationWizard.exe)

1. __Database__ - here you need to choose whether you want to create a new database or use an existing one. If this is your first time setting up the application choose 'Create new database'.
2. __Database Configuration__ - On the __Database Configuration__ wizard page specify the __SQL Server, Database Name__ and authentication. It is possible to overwrite the existing database under the same name. 
   - If you are using the default instance type  "servername", or "servername.yourdomain.loc"
   - If you are using a named instance type "servername\instancename", or "servername.yourdomain.loc\instancename"
   - If your SQL Server is on a non-standard port (different from 1433), type "severname,port" or "servername\instance,port". (FQDN formats are also supported)

    After providing the information, click the __Test Connection__ button to ensure that the settings are correct.
3. On the __Service Settings__ type the service account details. The service account needs to have the [following privileges](#internal/requirements/user-permissions-requirements) to be able to collect all the data from the desired servers.
4. __Insights Configuration__
    - **Index Location** – you need to ensure that the provided service account has write access to the index location directory. The directory for the index must be empty or contain an existing index.  It is recommended not to place the index on the system drive. Be careful if you plan to use the system drive for index location, as it can be quickly filled up.
    - **Port To Use** - this is the port that the Syskit Insight Agent will use to communicate with the Syskit Insights application. By default, port 7890 is set, but you can change it to suit your needs.
    - **Max Index Size** – by default we set this value to 200GB with a maximum of 1TB. Feel free to change it to suit your needs and hardware capabilities.
    If the service determines that the index exceeds the maximum index size, it will stop the data collection. Note that the actual size of the index can vary because of index reorganization and can require up to 3 times the amount of disk space specified here.
    
5. click __Next__ to complete the Configuration Wizard and apply the changes.

