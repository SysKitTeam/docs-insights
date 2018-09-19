---
title: Performance counters graphs are "incorrect".
description: Performance counters graphs are "incorrect" for a period when agent was sleeping.
author: Tomislav Sirovec
date: 23/01/2018
---

__Summary:__  
The problem appears when Syskit Insights is installed on a laptop, and when laptop is put into sleep mode. Personal computers (PCs) and servers (which does not have a sleep mode), are not affected by this. What happens, is that when you turn on the sleep mode, Syskit Insights Agent will "remember" the last collected value and "copy" it for every other performance data collection interval. There is no extra work done on a database so you do not have worry about that. The Agent starts to save new values the moment you turn on your laptop. 

![Laptop Sleeping](#img/laptop-sleeping-known-issue.png)

In the picture above the laptop was put into sleep mode at 16:00h and it was turned on the next morning at 08:00h

__Solution:__   
There is no workaround.