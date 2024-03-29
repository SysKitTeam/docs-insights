---
description: This article gives a basic overview of how to use Syskit Insights's Event Viewer.
---

# Event Viewer Dashboard

This article gives a basic overview of how to use Syskit Insights's Event Viewer.



![](../.gitbook/assets/event-viewer.png)

## Use Syskit Insights Event Viewer to search for events

1. Select the Event Viewer tab in the left navigation. 
2. Select the farm for which you wish to perform the search.
   * Selecting a farm is only available if multiple farms are used with the same  Syskit Insights database.
3. Select the time range in which to search for events.
   * Please limit the range as much as possible for optimal performance. 
   * First search will automatically be done with the "Last 10 Minutes" time interval. 
4. Enter your search query. Click [here](../how-to/search-query.md) for more details on writing a search query.
5. An empty query \(all events within the specified time range\) is also supported, but use sparingly, or on small time ranges. Just click search or press the enter key.

### Viewing results

By default, Syskit Insights uses a layout similar to a search engine to display the results. This layout can be changed to a more compact grid layout by using the dropdown button just below the search button. The results can also be exported to an Excel file.

### Refining your query

1. You can refine your query by:
   * Type of event \(ULS, Event Log, SQL\)
   * Additional refiners such as Server and Level are positioned to the left and will modify the query text.
   * Clicking on terms in the search results will also modify the query text.
     * for the compact grid layout expand the search result for this functionality to be available.
2. When satisfied with the constructed query, press the search button again.

### Alerts

You have created a very useful query and would like to be notified when an event that satisfied this query appears? No problem, just create an alert by clicking the alert button on the search results page. Click [here ](../how-to/manage-alerts.md)for more details.

