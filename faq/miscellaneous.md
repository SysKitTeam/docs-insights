---
description: A list of commonly asked questions.
---

# Miscellaneous

## When I use SPDocKit database to import farms, does the Syskit Insights application continue to use that database?

Once the farms are imported from the SPDocKit database, Syskit Insights does not continue to use it. Instead, Syskit Insights uses its own database. See [here ](../requirements/system-requirements.md)for system requirements.

## If I wish to monitor more than one farm do I need a database for each one?

No, Syskit Insights uses the **same database** to store information about every farm you wish to monitor.

## Does all index data go into the same index or are there different indexes for different farms?

Each Syskit Insights' agent can use only one index location.

## Are there installation instructions or best practices available for maximum index size?

It is very difficult to hypothesize on the required index size as this largely depends on your infrastructure and how big your farm/s are. Recommended minimum of 200GB disk space should be enough to store the data \(ULS, SQL logs and Windows Event logs\) of three SharePoint farms \(Test, Preproduction, Production\).  
**However, please note,** that index size can vary from a few gigabytes up to a terabyte of data depending on which Event Levels you are collecting and again, **on your infrastructure.** These Event Levels can be changed in [available farm settings](../how-to/customize-settings.md#available-farm-settings) in order to optimize the amount of collected data.

