---
title: System Requirements
description: >-
  This article discusses the hardware and software requirements that are 
  necessary in order to install the SysKit Insights.
author: Tomislav Sirovec
date: 17/01/2018
---

# System Requirements

## Software

* Microsoft Windows 7 \(with Service Pack 1\), Windows 8, Windows 8.1, Windows 10 or later are supported \(64-bit only\)
* **Windows Server** editions: Windows Server 2008 R2 – 2016, all editions
  * **Please note** that we do not recommend installing the application on a server which is part of a SharePoint farm.
  * In case of Windows Server 2008 R2 you will need the latest update for [Windows Management Framework](https://www.microsoft.com/en-us/download/details.aspx?id=54616). 
* Microsoft .NET Framework 4.5 or higher

## Hardware

* CPU – any Windows 7, Windows 8 or Windows 10 capable CPU with at least two cores
* Memory – 200 MB RAM while idle. Maximum RAM consumption depends on the workload and the number of monitored servers. 
* Disk – 250MB of available hard disk space
* Index – we recommend minimum of 200GB disk space required to store the index containing all the data \(ULS, SQL logs and Windows Event logs\). However, this largely depends on your infrastructure and how big your farm/s are. It is recommended to change the index location to a secondary drive.
* 1366×768 or higher resolution video card

## Database System

In order to run the SysKit Insights, you need a database. The SysKit Insights supports **SQL Server databases only**. SQL 2008 or better is supported.

User must have [proper privileges](user-permissions-requirements.md) to successfully run the application.

