# Customize Settings

To customize SysKit Insights settings click the **Settings button** located in the bottom left corner. 5. On the settings screen the available settings are divided into:

* General settings
* Farm settings scoped by each farm.
* Agent settings scoped by each agent.

## Available general settings

* **Email settings**
  * A list of settings required to send email notifications when alert occurs.

## Available farm settings:

* **Assigned agent**
  * When the SysKit Insights Agent starts for the first time, it will be associated with **all** the farms in your SysKit database. If at some point you connect another farm to your SysKit database, it will be associated with the first free active agent.
  * If the agent associated by default is not satisfactory, change this option.
  * If for some reason you wish to stop monitoring a farm, just select **None** as the desired agent.
  * One agent can be assigned to multiple farms. 
* **ULS collection configuration**
  * Here you can change which ULS event levels you want to collect. You can choose from the standard SharePoint ULS levels.
  * All of the ULS categories and sources are preselected by default.
* **Windows Event Log collection configuration**
  * Here you can change which Windows Event Levels and Logs you wish to monitor
  * Configure Windows event sources to monitor. By default SPDocKit, SharePoint and SQL are added. 
* **SQL collection configuration**
  * Enabled by default.
* **Performance monitoring**
  * Enabled by default.  
* **Intra-farm Latency Configuration**
  * Enabled by default.  
  * Ping response time threshold: 1ms by default
  * Ping rate above threshold tolerance: 0.1% by default

## Available agent options

* **Enable/Disable data collection**
  * Will stop/start data collection \(log and performance data\) from all farms associated with the selected SysKit Insights Agent.
* **Collection interval**
  * How often to collect log data \(default is 15 seconds\).
* **Data retention period** 
  * How long do you wish to keep the data \(default is 7 days for both Search and Performance\).
* **Max index size**
  * Data collection will stop when this limit is reached. 
* **Performance data collection interval**
  * How often to collect performance data \(default is 60 seconds\)
* **Remove agent** - only supported for an inactive agent.
  * Uninstall the selected SysKit Insights Agent form the machine where it is located.
  * You can do so by uninstalling SysKit Insights completely.
  * Wait a couple of minutes for the agent to register as offline.
  * Remove the agent by using this option.

