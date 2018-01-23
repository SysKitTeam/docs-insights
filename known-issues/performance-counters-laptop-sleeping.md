---
title: Performance counters graphs are "incorrect".
description: Performance counters graphs are "incorrect" for a period when agent was sleeping.
author: Tomislav Sirovec
date: 23/01/2018
---

__Summary:__ The problem appears when Syskit Insights is installed on a laptop, and when laptop is put into sleep mode. Personal computers (PCs) and servers (which does not have a sleep mode), are not affected by this. What happens, is that when you turn on the sleep mode, Syskit Insights Agent will "remember" the last collected value and "copy" it for every other performance data collection interval. There is no extra work done on a database so you do not have worry about that. 

__Solution:__ There is no workaround.