---
title: Performance counters graphs are "incorrect"
description: >-
  Performance counters graphs are "incorrect" for a period when agent was
  sleeping.
author: Tomislav Sirovec
date: 23/01/2018
---

# performance-counters-laptop-sleeping

**Summary:**  
The problem appears when Syskit Insights is installed on a laptop, and when laptop is put into sleep mode. Personal computers \(PCs\) and servers \(which does not have a sleep mode\), are not affected by this. What happens, is that when you turn on the sleep mode, Syskit Insights Agent will "remember" the last collected value and "copy" it for every other performance data collection interval. There is no extra work done on a database so you do not have worry about that. The Agent starts to save new values the moment you turn on your laptop.

![Laptop Sleeping](https://github.com/SysKitTeam/docs-insights/tree/e279e7cb077284447b4d0daa2f424e96e445e262/known-issues/#img/laptop-sleeping-known-issue.png)

In the picture above the laptop was put into sleep mode at 16:00h and it was turned on the next morning at 08:00h

**Solution:**  
There is no workaround.

