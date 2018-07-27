---
title: SysKit Insights Latency Screen
description: The SysKit Insights latency screen gives you an detailed overview of all the ping intervals we made.
author: Tomislav Sirovec
date: 24/07/2018
---

The SysKit Insights latency screen gives you an detailed overview of all the ping intervals we made.  

According to [Microsoft's guidelines](https://docs.microsoft.com/en-us/sharepoint/install/hardware-and-software-requirements) the Intra-farm latency should be <1 ms one way, 99.9% of the time over a period of ten minutes.  
Also, Microsoft defines Intra-farm latency as the latency between the front-end web servers and the database servers. But, we take it a step further and ping __every__ server in the farm. Not just the database server. 

On the left hand side of the screen, you can observe the success rate of sent pings to each monitored server. 

* __Success Rate__ column - gives you a number of successful pings for that server in the last interval. The interval will be displayed as critical if the ping success rate is not over 99.9%
* __Intra-farm Latency__ column - tells you if the latency for given server is according to the guidelines (99.9% of pings under 1ms in a 10 minute interval). 

On the right hand side there are __Server Interval Details.__  Click on any server and the data will appear. 

Pings are sent in 10 minute intervals.  
* __Sent Pings__ column gives you a number of sent/received pings.
* __Pings longer than 1 ms__ tells you how many of the pings took longer than 1ms. By default the value is set to 1 ms as per [Microsoft's guidelines.](https://docs.microsoft.com/en-us/sharepoint/install/hardware-and-software-requirements) However this can be changed in [settings](#internal/how-to/customize-settings) -> Intra-farm Latency Configuration
* __Maximum Latency__ tells you what was the maximum encountered latency in that interval. 