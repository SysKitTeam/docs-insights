---
title: SysKit Insights Frequently Asked Questions
description: A list of commonly asked questions. 
author: Tomislav Sirovec
date: 08/03/2018
---

This article lists some of the commonly asked questions. 

## When I use SPDocKit databased to import farms, does the SysKit Insights application continue to use that database?
Once the farms are imported from the SPDocKit database, SysKit Insights does not continue to use it. Instead, SysKit Insights uses its own database. See [here](#internal/requirements/system-requirements) for system requirements.

## If I wish to monitor more then one farm do I need a database for each one?
No, SysKit Insights uses the __same database__ to store information about every farm you wish to monitor. 

## Does all index data go into the same index or are there different indexes for different farms?
Each SysKit Insights' agent can uses only one index location. 

## Are there installation instructions or best practices available for maximum index size? 
It is very difficult to hypothesize on the required index size as this largely depends on your infrastructure and how big your farm/s are. Recommended minimum of 200GB disk space should be enough to store the data (ULS, SQL logs and Windows Event logs) of three SharePoint farms (Test, Preproduction, Production).  
__However, please note,__ that index size can vary from a few gigabytes up to a terabyte of data depending on which Event Levels you are collecting and again, __on your infrastructure.__