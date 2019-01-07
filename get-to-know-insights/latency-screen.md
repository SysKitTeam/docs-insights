---
title: SysKit Insights Latency Screen
description: The SysKit Insights latency screen gives you a detailed overview of all the ping intervals made.
author: Tomislav Sirovec
date: 24/07/2018
---

The SysKit Insights latency screen gives you a detailed overview of all the ping intervals recorded.

According to [Microsoft's guidelines](https://docs.microsoft.com/en-us/sharepoint/install/hardware-and-software-requirements), intra-farm latency should be <1 ms one way 99.9% of the time over a period of ten minutes.
Microsoft defines Intra-farm latency as the latency between the front-end web servers and the database servers. However, we take it a step further and ping __every__ server in the farm, not just the database server.

On the left side of the screen, you can observe the success rate of pings sent to each monitored server.

* __Success Rate__ column: Gives you the number of successful pings for that server in the last interval. The interval will be displayed as critical if the ping success rate is not over 99.9%.
* __Intra-farm Latency__ column: Tells you if the latency for given server is according to the guidelines (99.9% of pings under 1 ms in a 10-minute interval).

On the right side are __server interval details__. Click on any server and its data will appear.

Pings are sent in 10-minute intervals.
* The __Sent Pings__ column gives you the number of sent/received pings.
* __Pings longer than 1 ms__ tells you how many pings took longer than 1 ms. By default, the value is set to 1 ms per [Microsoft's guidelines.](https://docs.microsoft.com/en-us/sharepoint/install/hardware-and-software-requirements). This can be changed in [Settings](#internal/how-to/customize-settings) -> Intra-farm Latency Configuration
* __Maximum Latency__ tells you the maximum encountered latency in that interval.