---
description: The SysKit Insights latency screen gives you a detailed overview of all the ping intervals made.
---

# Latency Screen

According to [Microsoft's guidelines](https://docs.microsoft.com/en-us/sharepoint/install/hardware-and-software-requirements), intra-farm latency should be &lt;1 ms one way 99.9% of the time over a period of ten minutes. Microsoft defines Intra-farm latency as the latency between the front-end web servers and the database servers. However, we take it a step further and ping **every** server in the farm, not just the database server.

On the left side of the screen, you can observe the success rate of pings sent to each monitored server.

* **Success Rate** column: Gives you the number of successful pings for that server in the last interval. The interval will be displayed as critical if the ping success rate is not over 99.9%.
* **Intra-farm Latency** column: Tells you if the latency for given server is according to the guidelines \(99.9% of pings under 1 ms in a 10-minute interval\).

On the right side are **server interval details**. Click on any server and its data will appear.

Pings are sent in 10-minute intervals.

* The **Sent Pings** column gives you the number of sent/received pings.
* **Pings longer than 1 ms** tells you how many pings took longer than 1 ms. By default, the value is set to 1 ms per [Microsoft's guidelines.](https://docs.microsoft.com/en-us/sharepoint/install/hardware-and-software-requirements). This can be changed in [Settings](../how-to/customize-settings.md) -&gt; Intra-farm Latency Configuration
* **Maximum Latency** tells you the maximum encountered latency in that interval.

