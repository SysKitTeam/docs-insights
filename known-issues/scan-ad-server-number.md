---
title: CREATE TABLE permissions denied
description: Number of processed servers during the scan is incorrect.
author: Tomislav Sirovec
date: 17/01/2018
---

__Summary:__ The problem may appear when scanning a certain Organizational Unit(OU).  
 For example if you have an OU named SharePointFarm with 7 SharePoint servers, but a SQL server is located in another OU. The message during the scan will say: "Processed: x out of 7 servers." While in fact the number of discovered servers will be 8 (because of the SQL server).  

__Solution:__ There is no workaround. 