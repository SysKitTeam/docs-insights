---
title: System Requirements
description: This article discusses the hardware and software requirements that are necessary in order to install the SysKit Insights.
author: Tomislav Sirovec
date: 17/01/2018
---

## Software
* Microsoft Windows 7 (with Service Pack 1), Windows 8, Windows 8.1, Windows 10 or later are supported (64-bit only)
* __Windows Server__ editions: Windows Server 2008 R2 – 2016, all editions
    * __Please note__ that we do not recommend installing the application on a server which is part of a SharePoint farm.
* Microsoft .NET Framework 4.5 or higher


## Hardware

* CPU – any Windows 7, Windows 8 or Windows 10 capable CPU with at least two cores
* Memory – up to 512 MB (200 MB RAM while idle)
* Disk – 250MB of available hard disk space
* Index – we recommend minimum of 200GB disk space required to store the index containing all the data (ULS, SQL logs and Windows Event logs). However, this largely depends on your infrastructure and how big your farm/s are. It is recommended to change the index location to a secondary drive.
* 1366×768 or higher resolution video card


## Database System

In order to run the SysKit Insights, you need a database. The SysKit Insights supports __SQL Server databases only__. SQL 2008 or better is supported.  


User must have [proper privileges](#internal/requirements/user-permissions-requirements) to successfully run the application.