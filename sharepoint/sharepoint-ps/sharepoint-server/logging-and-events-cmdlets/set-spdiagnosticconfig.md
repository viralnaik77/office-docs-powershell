---
title: "Set-SPDiagnosticConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b6026e1-ef05-4c88-908b-2aed041bcb06

description: "Sets diagnostic configuration settings on the farm."
---

# Set-SPDiagnosticConfig

Sets diagnostic configuration settings on the farm.
  
```
Set-SPDiagnosticConfig [-AllowLegacyTraceProviders <SwitchParameter>] [-AppAnalyticsAutomaticUploadEnabled <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-CustomerExperienceImprovementProgramEnabled <SwitchParameter>] [-DaysToKeepLogs <Int32>] [-DownloadErrorReportingUpdatesEnabled <SwitchParameter>] [-ErrorReportingAutomaticUploadEnabled <SwitchParameter>] [-ErrorReportingEnabled <SwitchParameter>] [-EventLogFloodProtectionEnabled <SwitchParameter>] [-EventLogFloodProtectionNotifyInterval <Int32>] [-EventLogFloodProtectionQuietPeriod <Int32>] [-EventLogFloodProtectionThreshold <Int32>] [-EventLogFloodProtectionTriggerPeriod <Int32>] [-InputObject <PSObject>] [-LogCutInterval <Int32>] [-LogDiskSpaceUsageGB <Int32>] [-LogLocation <String>] [-LogMaxDiskSpaceUsageEnabled <SwitchParameter>] [-ScriptErrorReportingDelay <Int32>] [-ScriptErrorReportingEnabled <SwitchParameter>] [-ScriptErrorReportingRequireAuth <SwitchParameter>]
```

## Detailed Description

Use the **Set-SPDiagnosticConfig** cmdlet to set diagnostic configuration settings on the entire farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AllowLegacyTraceProviders** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that trace providers built for previous versions of SharePoint Products and Technologies can write to the trace session for SharePoint 2010 Products.  <br/> |
|**AppAnalyticsAutomaticUploadEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether aggregated app usage data is automatically uploaded to Microsoft.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CustomerExperienceImprovementProgramEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether participation in the Customer Experience Improvement Program (CEIP) is enabled.  <br/> The CEIP is designed to improve the quality, reliability, and performance of Microsoft products and technologies. With your permission, anonymous information about your server is sent to Microsoft to help improve SharePoint 2010 Products.  <br/> The type must be either of the following values:  <br/> - **$True** <br/> - **$False** <br/> The default value is **$True**.  <br/> |
|**DaysToKeepLogs** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of days to keep trace log files. The type must be a valid number between 1 and 366. The default value is 14 days..  <br/> |
|**DownloadErrorReportingUpdatesEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether the error reporting remote control file is downloaded.  <br/> The type must be either of the following values:  <br/> - **$True** <br/> - **$False** <br/> The default value is **$True**.  <br/> |
|**ErrorReportingAutomaticUploadEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether error reports are uploaded to Microsoft automatically.  <br/> Error reports include the following: information regarding the condition of the server when a problem occurs; the operating system version and computer hardware in use; and the digital product ID, which can be used to identify your license. The IP address of your computer is also sent because you are connecting to an online service to send error reports; however, the IP address is used only to generate aggregate statistics.  <br/> The type must be either of the following values:  <br/> - **$True** <br/> - **$False** <br/> The default value is **$True**.  <br/> |
|**ErrorReportingEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether collection of error reports is enabled.  <br/> Error reports are created when your system encounters hardware or software problems. Microsoft and its partners actively use these reports to improve the reliability of the software. Error reports include the following: information regarding the condition of the server when the problem occurs; the operating system version and computer hardware in use; and the digital product ID, which can be used to identify your license. The IP address of your computer is also sent because you are connecting to an online service to send error reports; however, the IP address is used only to generate aggregate statistics.  <br/> The type must be either of the following values:  <br/> - **$True** <br/> - **$False** <br/> The default value is **$True**.  <br/> |
|**EventLogFloodProtectionEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether the Event log flood protection feature is enabled.  <br/> If multiple similar events are written to the event log, some duplicate messages are suppressed. Then, after a period of time, a summary message is written that shows how many events were suppressed.  <br/> The type must be either of the following values:  <br/> - **$True** <br/> - **$False** <br/> The default value is **$True**.  <br/> |
|**EventLogFloodProtectionNotifyInterval** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies in minutes how often to write a summary event indicating how many events were suppressed due to flood protection.  <br/> The integer range is between 1 and 1440. The default value is **5**.  <br/> |
|**EventLogFloodProtectionQuietPeriod** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies in minutes how much time must pass without an event firing to exit flood protection.  <br/> The integer range is between 1 and 1440. The default value is **2**.  <br/> |
|**EventLogFloodProtectionThreshold** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of events allowed in a given timeframe before an event is considered to be flooding the event log.  <br/> The integer range is between 1 and 100. The default value is **5**.  <br/> |
|**EventLogFloodProtectionTriggerPeriod** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies in minutes the timeframe to watch for events that may be flooding.  <br/> The integer range is between 1 and 1440. The default value is **2**.  <br/> |
|**InputObject** <br/> |Optional  <br/> |System.Management.Automation.PSObject  <br/> |Use the result from the **Get-SPDiagnosticConfig** cmdlet, make modifications, and then pipeline the object into **Set-SPDiagnosticConfig** cmdlet to update the content database.  <br/> |
|**LogCutInterval** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies a time period to roll over to the next log file.  <br/> The type must be a valid number between 0 and 1440.  <br/> The default value is **30**.  <br/> |
|**LogDiskSpaceUsageGB** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum amount of storage to use for trace log files, in gigabytes (GB).  <br/> The default value is 1000 and only takes effect when the **LogMaxDiskSpaceusageEnabled** cmdlet is set to True.  <br/> The type must be a valid number between 1 and 1000.  <br/> |
|**LogLocation** <br/> |Optional  <br/> |System.String  <br/> |Specifies the path of where to log files will reside.  <br/> The type must be a valid path, in the form C:\Logs.  <br/> The default location is %CommonProgramFiles%\Microsoft Shared\Web Server Extensions\14\Logs.  <br/> |
|**LogMaxDiskSpaceUsageEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to restrict the maximum space to use for trace log files.  <br/> The type must be either of the following values:  <br/> - **$True** <br/> - **$False** <br/> The default value is **$False**.  <br/> |
|**ScriptErrorReportingDelay** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the time (in minutes) between script error reports.  <br/> The type must be a valid integer between 0 and 1440. The value is specified in minutes.  <br/> The default value is **30**.  <br/> |
|**ScriptErrorReportingEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether error reporting is enabled for client script errors.  <br/> The type must be either of the following values:  <br/> - **$True** <br/> - **$False** <br/> The default value is **$True**.  <br/> |
|**ScriptErrorReportingRequireAuth** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether script error reporting requires authentication.  <br/> The type must be either of the following values:  <br/> - **$True** <br/> - **$False** <br/> The default value is **$True**.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AllowLegacyTraceProviders** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AppAnalyticsAutomaticUploadEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CustomerExperienceImprovementProgramEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DaysToKeepLogs** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**DownloadErrorReportingUpdatesEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ErrorReportingAutomaticUploadEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ErrorReportingEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**EventLogFloodProtectionEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**EventLogFloodProtectionNotifyInterval** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**EventLogFloodProtectionQuietPeriod** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**EventLogFloodProtectionThreshold** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**EventLogFloodProtectionTriggerPeriod** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**InputObject** <br/> |Optional  <br/> |System.Management.Automation.PSObject  <br/> ||
|**LogCutInterval** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**LogDiskSpaceUsageGB** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**LogLocation** <br/> |Optional  <br/> |System.String  <br/> ||
|**LogMaxDiskSpaceUsageEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ScriptErrorReportingDelay** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**ScriptErrorReportingEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ScriptErrorReportingRequireAuth** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1-----------------------
  
```
set-spdiagnosticconfig -errorReportingEnable -DownloadErrorReportingUpdatesEnabled:$false -DaysToKeepLog  60
```

This example enables ErrorReporting, disables DownloadErrorReportingUpdatesEnable, and sets DaysToKeepLog to  `60`. 
  
------------------EXAMPLE 2-----------------------
  
```
$L = get-spdiagnosticconfig
```

```
$L.CustomerExperienceImprovementProgramEnabled = $false
```

```
$L.LogCutInterval = 60
```

```
$L | Set-SPDiagnosticConfig
```

This example disables CEIP and sets LogCutInterval to  `60` minutes. 
  
## See also

#### 

[Get-SPDiagnosticConfig](get-spdiagnosticconfig.md)

