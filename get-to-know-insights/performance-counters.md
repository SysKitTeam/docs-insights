---
title: Performance Counters help
description: >-
  Performance Counters help page offers you a list of all the available counters
  along with their thresholds.
author: Tomislav Sirovec
date: 02/02/2018
---

# performance-counters

SysKit Insights monitors your server performance by periodically collecting performance counter values. The counters are split into several templates that are applied to your server based on the role it plays in your farm.

Most counters have a critical and warning threshold defined. When the counter value remains above the threshold for an extended period of time it will be classified with a critical or warning status. This in turn will affect the status of the server seen on the dashboards and it will cause an Alert to be sent - if you have that [option](performance-counters.md#internal/how-to/manage-alerts) turned on.  
Please note that these threshold can be changed to suit your needs more reliably.

See [this article](https://technet.microsoft.com/en-us/library/bb734903.aspx?f=255&MSPPError=-2147217396) for some guidelines on performance testing and tuning.

Below are the counters that SysKit tracks with their corresponding \(default\) critical and warning thresholds.

## **General**

Default template contains counters that are collected for all servers.

### % Processor Time

% Processor Time is the percentage of elapsed time that all of process threads used the processor to execution instructions. An instruction is the basic unit of execution in a computer, a thread is the object that executes instructions, and a process is the object created when a program is run. Code executed to handle some hardware interrupts and trap conditions are included in this count.

Warning when the value is above 85%. Critical when the value is above 95%.

### RAM \(GB\)

Displays the amount of used memory, in GB, on a computer.

Warning when there is less than 0.5 GB available. Critical when there is less than 0.25 GB available.

### Network Usage \(Kbps\)

Number of kilobits received and sent per second on the network adapter.

Warning when the value is above 5000 Kbps. Critical when the value is above 10000 Kbps.

### Disk I/O \(bytes/sec\)

Number of bytes read from and written to the disk per second.

Warning when the value is above 100 bytes/sec. Critical when the value is above 200 bytes/sec.

## **IIS/ASP.NET**

IIS/ASP.NET template helps you keep an eye on your IIS servers in SharePoint farm. Diagnose various problems and performance issues with ease.

### Current Connections

Current Connections is the current number of connections established with the Web service.

### Bytes Total/sec

Bytes Total/sec is the sum of Bytes Sent/sec and Bytes Received/sec. This is the total rate of bytes transferred by the Web service.

### Get Requests/sec

The rate HTTP requests using the GET method are made. Get requests are the most common HTTP request.

### Post Requests/sec

The rate HTTP requests using the POST method are made.

### Total Application Pool Recycles

The number of times that the application pool has been recycled since Windows Process Activation Service \(WAS\) started.

### Requests Queued

The number of requests waiting to be processed.

Warning when the value is above 400. Critical when the value is above 1000.

### Requests Rejected

The number of requests rejected because the request queue was full.

Warning when the value is above 2. Critical when the value is above 5.

### Worker Process Restarts

Number of times a worker process has restarted on the machine.

Warning when the value is above 1. Critical when the value is above 5.

### Request Wait Time

The number of milliseconds the most recent request was waiting in the queue.

Warning when the value is above 800. Critical when the value is above 1200.

## **SQL**

SQL template enables you to efficiently monitor your SQL servers. With specified counters you can quickly find possible bottlenecks and performance issues.

### User Connections

Number of users connected to the system.

### Buffer Cache Hit Ratio \(%\)

Percentage of pages that were found in the buffer pool without having to incur a read from disk.

Warning when the value is below 90. Critical when the value is below 80.

### Lazy Writes/sec

Number of buffers written by buffer manager's lazy writer.

Warning when the value is above 15. Critical when the value is above 20.

### Page Life Expectancy \(s\)

Number of seconds a page will stay in the buffer pool without references.

Warning when the value is below 400. Critical when the value is below 250.

### Batch Requests/sec

Number of SQL batch requests received by server.

Warning when the value is above 1000. Critical when the value is above 1500.

### SQL Compilations/sec

Number of SQL compilations.

Warning when the value is above 100. Critical when the value is above 150.

### SQL Re-Compilations/sec

Number of SQL re-compiles.

Warning when the value is above 1. Critical when the value is above 2.

### Page Splits/sec

Number of page splits per second that occur as a result of overflowing index pages.

Warning when the value is above 200. Critical when the value is above 300.

### Full Scans/sec

Number of unrestricted full scans. These can either be base table or full index scans.

### Latch Waits/sec

Number of latch requests that could not be granted immediately and had to wait before being granted.

### Total Latch Wait Time \(ms\)

Total latch wait time \(milliseconds\) for latch requests that had to wait in the last second.

### Lock Waits/sec

Number of lock requests that could not be satisfied immediately and required the caller to wait before being granted the lock.

Warning when the value is above 1. Critical when the value is above 2.

### Transactions/sec

Number of transactions started for the database.

### Processor Queue Length

Processor Queue Length is the number of threads in the processor queue. Unlike the disk counters, this counter shows ready threads only, not threads that are running. There is a single queue for processor time even on computers with multiple processors. Therefore, if a computer has multiple processors, you need to divide this value by the number of processors servicing the workload. A sustained processor queue of greater than two threads generally indicates processor congestion.

Warning when the value is above 2. Critical when the value is above 5.

## **Disk**

Disk template helps you keep an eye on your disks across the SharePoint farm. Diagnose possible bottlenecks and performance issues with ease.

### Avg. Disk Queue Length

Avg. Disk Queue Length is the average number of both read and write requests that were queued for the selected disk during the sample interval.

Warning when the value is above 2. Critical when the value is above 4.

### Disk Transfers/sec

Disk Transfers/sec is the rate of read and write operations on the disk.

Warning when the value is above 200 transfers/sec. Critical when the value is above 400 transfers/sec.

### Free GB

Free GB displays the unallocated space on the disk drive in GB.

Warning when the value is below 5 GB. Critical when the value is below 3 GB.

### Pages/sec

Pages/sec is the rate at which pages are read from or written to disk to resolve hard page faults. This counter is a primary indicator of the kinds of faults that cause system-wide delays. It is the sum of Memory\Pages Input/sec and Memory\Pages Output/sec. It is counted in numbers of pages, so it can be compared to other counts of pages, such as Memory\Page Faults/sec, without conversion. It includes pages retrieved to satisfy faults in the file system cache \(usually requested by applications\) non-cached mapped memory files.

Warning when the value is above 20. Critical when the value is above 50.

### Disk Reads/sec

Disk Reads/sec is the rate of read operations on the disk.

### Avg. Disk Read Queue Length

Avg. Disk Read Queue Length is the average number of read requests that were queued for the selected disk during the sample interval.

### Avg. Disk Write Queue Length

Avg. Disk Write Queue Length is the average number of write requests that were queued for the selected disk during the sample interval.

### % Idle Time

% Idle Time reports the percentage of time during the sample interval that the disk was idle.

Warning when the value is below 20. Critical when the value is below 10.

### % Free Space

% Free Space is the percentage of total usable space on the selected logical disk drive that was free.

Warning when the value is below 30. Critical when the value is below 20.

### Cache Faults/sec

Cache Faults/sec is the rate at which faults occur when a page sought in the file system cache is not found and must be retrieved from elsewhere in memory \(a soft fault\) or from disk \(a hard fault\). The file system cache is an area of physical memory that stores recently used pages of data for applications. Cache activity is a reliable indicator of most application I/O operations. This counter shows the number of faults, without regard for the number of pages faulted in each operation.

Critical when the value is above 1.

### % Usage

The amount of the Page File instance in use in percent. See also Process\Page File Bytes.

Warning when the value is below 50. Critical when the value is below 75.

### % Usage Peak

The peak usage of the Page File instance in percent. See also Process\Page File Bytes Peak.

### Total Bytes/sec

Total Bytes/sec is the rate the Server is reading and writing data to and from the files for the clients on this CPU. This value is a measure of how busy the Server is.

### Page Reads/sec

Page Reads/sec is the rate at which the disk was read to resolve hard page faults. It shows the number of reads operations, without regard to the number of pages retrieved in each operation. Hard page faults occur when a process references a page in virtual memory that is not in working set or elsewhere in physical memory, and must be retrieved from disk. This counter is a primary indicator of the kinds of faults that cause system-wide delays. It includes read operations to satisfy faults in the file system cache \(usually requested by applications\) and in non-cached mapped memory files. Compare the value of Memory\Pages Reads/sec to the value of Memory\Pages Input/sec to determine the average number of pages read during each operation.

## **.NET**

.NET template helps you track .NET counters on servers in SharePoint farm. Diagnose various problems and performance issues with ease.

### Gen 0 Collections

This counter displays the number of times the generation 0 objects \(youngest most recently allocated\) are garbage collected \(Gen 0 GC\) since the start of the application. Gen 0 GC occurs when the available memory in generation 0 is not sufficient to satisfy an allocation request. This counter is incremented at the end of a Gen 0 GC. Higher generation GCs include all lower generation GCs. This counter is explicitly incremented when a higher generation \(Gen 1 or Gen 2\) GC occurs. _Global_ counter value is not accurate and should be ignored. This counter displays the last observed value.

### Gen 1 Collections

This counter displays the number of times the generation 1 objects are garbage collected since the start of the application. The counter is incremented at the end of a Gen 1 GC. Higher generation GCs include all lower generation GCs. This counter is explicitly incremented when a higher generation \(Gen 2\) GC occurs. _Global_ counter value is not accurate and should be ignored. This counter displays the last observed value.

### Gen 2 Collections

This counter displays the number of times the generation 2 objects \(older\) are garbage collected since the start of the application. The counter is incremented at the end of a Gen 2 GC \(also called full GC\). _Global_ counter value is not accurate and should be ignored. This counter displays the last observed value.

% Time in GC % Time in GC is the percentage of elapsed time that was spent in performing a garbage collection \(GC\) since the last GC cycle. This counter is usually an indicator of the work done by the Garbage Collector on behalf of the application to collect and compact memory. This counter is updated only at the end of every GC and the counter value reflects the last observed value its not an average.

## **Search**

Search templates helps you track a number of 'search' relevant counters on servers in SharePoint farm. Diagnose various problems and performance issues with ease.

### Retries

The total number of times a document access has been retried. Having this number high may indicate a problem with accessing the data.

### Crawls in progress

Number of crawls in progress.

### Transactions Completed

Shows the current number of completed documents in the transactions queue.

### Transactions Waiting

The number of documents waiting to be processed. When this number goes to zero the catalogue is idle. This number indicates the total queue size of unprocessed documents in the gatherer.

### Transactions In Progress

The number of documents in progress.

### Documents Processed Rate

The number of documents processed per second.

### Documents Success Rate

The number of successfully filtered documents per second.

