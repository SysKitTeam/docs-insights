---
title: SharePoint Online Page Performance
description: How to use SysKit Insights to monitor a SPO page. 
author: Tomislav Sirovec
date: 25/10/2018
---

This article will describe how to use SysKit Insights to __monitor a SharePoint Online's page performance__. 

If you do not have any on-premises farms, and you only wish to monitor page performance of your SharePoint Online (SPO) pages, this is what you need to do:

1. When you install and start the application, __Farms tab__ will automatically open. Since you do not have any on-premise farms click the button that says: Use SysKit Insights to monitor SharePoint Online.
2. You will be automatically redirected to Page Performance's __Add Page screen__.
3. Once there, simply input the URL of a page you wish to monitor, or you can import them from a file. When importing from a file, separate the pages with a newline.
4. Click __Import__ and the import check will start. A pop up window will ask you to give consent and provide credentials.  When prompted to remember the login make sure to click __yes__. The benefits are:
    - Credentials will be reused for all connections to the same tenant.
    - The credentials will be valid for more than 5 days.

After adding all the pages you wish, they will be shown on the Page Performance dashboard.

And that is it. For more general information on Page Performance feature see [this article.](#internal/get-to-know-insights/page-performance-screen#page-performance-dashboard)