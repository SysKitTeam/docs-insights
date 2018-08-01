---
title: SysKit Insights Performance 
description: Starting with version 1.1, SysKit Insights includes a web interface. It enables users to access all the functions of SysKit Insights using any web browser.
author: Hrvoje Bagarić
date: 28/07/2018
---

Starting with version 1.1, SysKit Insights includes a web interface. It enables users to access all the functions of SysKit Insights using any web browser.

## SysKit Insights Web Interface 

SysKit Insights Configuration Wizard has a separate step where users can configure the SysKit Insights web interface. Users can choose to enable it or disable it completely. Additionally, users can define which user accounts can access the SysKit Insights web interface. By default, only the user account running the Configuration Wizard and service user account are added to the group of users with permission to access the SysKit Insights web interface. Users can add unlimited user accounts to this group. The people picker will search Active Directories for the users. 

The SysKit Insights web interface is hosted at http://{servername}:{port} or at https://{servername}:{port}. In order to use https, the user must set up the certificate manually. You can follow the steps [here](#internal/how-to/set-up-https).

## Browser Compatibility

SysKit Inisghts has only been tested on the latest version of Google Chrome but should also work on the latest versions of Microsoft Edge, Mozilla Firefox, and Safari.


