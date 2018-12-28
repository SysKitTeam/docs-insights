---
title: Page Performance via Web App
description: >-
  SysKit Insights cannot add certain (SharePoint Online) pages when using the
  web application.
author: Tomislav Sirovec
date: 22/10/2018
---

# webapp-page-performance

**Summary:**  
The problem appears when the user is using the web application to add a site for which he/she does not have permission. In most cases, this will happen with a SPO \(SharePoint Online\) site. To be more precise, the problem lies with the authentication process for the given site. If you already have the required permissions, eg. for a on-premise site, you should be able to add the given site.

**Solution:**  
You should always use the SysKit Insights **desktop application** when adding new pages for [Page Performance](webapp-page-performance.md#internal/get-to-know-insights/page-performance-screen) monitoring.

