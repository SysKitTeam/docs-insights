---
description: How to use SysKit Insights to monitor a SPO page.
---

# SharePoint Online Page Performance

If you do not have any on-premises farms and you want to monitor the performance of your SharePoint Online \(SPO\) pages only, this is what you need to do:

1. When you install and start the application, the farms tab will automatically open. Since you do not have any on-premises farms, click the button “Use SysKit Insights to monitor SharePoint Online.”
2. You will be automatically redirected to the **add page screen of Page Performance**.
3. Once there, simply input the URL of a page you want to monitor or import URLs from a file. When importing from a file, put each page on a separate line.
4. Click **Import** and the import check will start. A pop-up window will ask you to give consent and to provide your credentials. When prompted to “remember the login” make sure to click **yes**. The benefits are:
   * Credentials will be reused for all connections to the same tenant.
   * The credentials will be valid for more than 5 days.

After adding all the pages you wish, they will be shown on the Page Performance dashboard.

And that is it. For more general information on the Page Performance feature, please see [this article.](../get-to-know-insights/page-performance-screen.md#page-performance-dashboard)

{% hint style="warning" %}
**Please note!** This process of adding a SPO "farm" is required due to restrictions in how our application works. The pages you wish to monitor must "belong" to a farm. When importing pages, if you already have an on-premises farm, it is fine to "put them" into an existing on-premises farm. In this instance, the farm is merely an abstract container.
{% endhint %}

