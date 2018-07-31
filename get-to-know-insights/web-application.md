---
title: SysKit Insights Performance 
description: Detailed overview on how the SysKit Insights collects and presents farm performance data.
author: Hrvoje Bagarić
date: 28/07/2018
---

From version 1.1. SysKit Insights comes with the web interface. It enables users to access fully functional SysKit Insights using any web browser. 

## SysKit Insights Web Interface 

SysKit Insights Configuration Wizard has a separate step where users can configure SysKit Insights web interface. Users can choose to enable it or disable it completely. Additionally, users can define which user accounts can access SysKit Insights web interface. By default, only the user account running the Configuration Wizard and service user account are added to the group of users with permissions to access SysKit Insights web interface. Users can add unlimited additional user accounts. The people picker will search Active Directories for the users. 

The SysKit Insights web interface is hosted at http://{servername}:{port} and at https://{servername}:{port}. In order to use https the user have to set it up certificate manually. You can follow the steps [here](#internal/how-to/set-up-https).

## Browser Compatibility

SysKit Inisghts is tested only on the latest version of Google Chrome but should work also on the latest versions of Microsoft Edge, Mozilla Firefox, Safari.

