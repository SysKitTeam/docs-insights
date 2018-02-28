---
title: Performance Counters Best Practices
description: This article provides guidelines for performance testing and tuning. 
author: Tomislav Sirovec
date: 28/02/2018
---

> Pleased note that, as they are subject to change, thresholds are not stated in this article.

Categorie | Counter | Comment
:---------:|:--------:|:-------
General | % Processor Time | Isolate the process that is using a high percentage of processor time. Upgrade to a faster processor, or install an additional processor.
General | RAM (GB) | Research memory usage, and then add memory, if needed.
General | Network Kb Total/sec (Received and Sent) | Use to determine if your network connection is creating a bottleneck. Compare this counter to the total band-width of your network adapter. You should be using no more than 50 percent of the network adapter capacity.
fgf | fds | proba proba, work in progress
