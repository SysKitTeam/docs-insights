---
description: Number of processed servers during the scan is incorrect.
---

# Scanning the AD

## **Summary**

  
The problem may appear when scanning a certain Organizational Unit\(OU\).  
For example if you have an OU named SharePointFarm with 7 SharePoint servers, but a SQL server is located in another OU. The message during the scan will say: "Processed: x out of 7 servers." While in fact the number of discovered servers will be 8 \(because of the SQL server\).

## **Solution**

  
After the discovery process is finished go to the **Alerts tab -&gt; click Manage.** Locate the Farm in which you have missing servers -&gt; click **Add Server** and manually add the missing server. You will need to provide a Server Name and a Server Role\(s\). For more information on how to do this see [this article.](../get-to-know-insights/farms-screen.md)

