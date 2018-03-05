---
title: "Merge-SPLogFile"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 759702d7-bda2-4302-9345-abb43b609ad4

description: "Combines trace log entries from all farm computers into a single log file on the local computer."
---

# Merge-SPLogFile

Combines trace log entries from all farm computers into a single log file on the local computer.
  
```
Merge-SPLogFile -Path <String> [-Area <String[]>] [-AssignmentCollection <SPAssignmentCollection>] [-Category <String[]>] [-ContextFilter <String[]>] [-Correlation <Guid[]>] [-EndTime <DateTime>] [-EventID <String[]>] [-ExcludeNestedCorrelation <SwitchParameter>] [-Level <String>] [-Message <String[]>] [-Overwrite <SwitchParameter>] [-Process <String[]>] [-StartTime <DateTime>] [-ThreadID <UInt32[]>]
```

## Detailed Description

The **Merge-SPLogFile** cmdlet returns records from Unified Logging Service (ULS) trace log files on each farm server that match the criteria, and writes the results to a new log file on the local computer. If no results are returned, a warning is written to the Microsoft PowerShell console window. 
  
We recommend that you filter by using the **StartTime** and **EndTime** parameters to optimize performance of this cmdlet. Some filtering parameters such as **Process**, **Area**, **Category**, **EventID** and **Message** support wildcards. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the path and file name to which to write the merged log file. Relative paths are supported.  <br/> |
|**Area** <br/> |Optional  <br/> |System.String  <br/> |Specifies the area name to filter on.  <br/> The type must be a valid name; for example, SharePoint Server 2016.  <br/> The use of wildcards is supported.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Category** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies the category ID to filter on.  <br/> The type must be a valid category name; for example, category1.  <br/> The use of wildcards is supported.  <br/> |
|**ContextFilter** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies a filter for trace entries in a particular context in the form key=value, for example, user=contoso\joeuser.  <br/> |
|**Correlation** <br/> |Optional  <br/> |System.Guid[]  <br/> |Specifies the correlation ID to filter on. The type must be a valid GUID, in the form F0BB0790-4323-A153-096F-ABCDC80E24D4.  <br/> |
|**EndTime** <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the end time of the log entries returned.  <br/> The type must be a valid DateTime format that is culture-specific to the administrative language, such as 2/16/2007 12:15:12 for English-US.  <br/> |
|**EventID** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies the Event ID to filter on. The use of wildcards is supported.  <br/> |
|**ExcludeNestedCorrelation** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Excludes nested correlation values in the results. This parameter is only used when filtering results by using the **ContextFilter** parameter  <br/> By default, records returned from the **ContextFilter** parameter include all related records in addition to the records that match the filter. Specifying this option includes only the records that match the filter and excludes any related records.  <br/> |
|**Level** <br/> |Optional  <br/> |System.String  <br/> |Specifies the level name to filter on.  <br/> Results include the specified level and everything more severe.  <br/> The valid values are (in order of severity): **Information**, **Medium**, **High**, **Verbose**, **VerboseEx**, **Monitorable**, **Warning**, **Error**, **Critical**, or **Unassigned**.  <br/> |
|**Message** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies the message text to filter on.  <br/> The type must be valid text. Text with spaces should be enclosed with quotation marks; for example, "This is a test."  <br/> The use of wildcards is supported.  <br/> |
|**Overwrite** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Overwrites the log file if it already exists at the specified path.  <br/> The type must be either of the following values:  <br/> - **$True** <br/> - **$False** <br/> The default value is **$False**.  <br/> |
|**Process** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies the process name to filter on.  <br/> The use of wildcards is supported.  <br/> |
|**StartTime** <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the start time of the log entries returned.  <br/> The type must be a valid DateTime format that is culture-specific to the administrative language, such as 2/16/2007 12:15:12 for English-US.  <br/> The default is one hour prior to the current time on the local computer.  <br/> |
|**ThreadID** <br/> |Optional  <br/> |System.UInt32[]  <br/> |Specifies the thread ID to filter on.  <br/> The type must be a valid integer from 0 through 4,294,967,295.  <br/> |
   
## Example

--------------EXAMPLE 1-----------------
  
```
Merge-SPLogFile -Path "C:\Logs\FarmMergedLog.log" -Overwrite
```

This example merges the last hour of log data from all farm computers with no filtering.
  
--------------EXAMPLE 2-----------------
  
```
Merge-SPLogFile -Path "C:\Logs\FarmMergedLog.log" -Overwrite -Area Search
```

This example merges the last hour of log data from the  `Search` area. 
  
--------------EXAMPLE 3-----------------
  
```
Merge-SPLogFile -Path "C:\Logs\FarmMergedLog.log" -Overwrite -Area "SharePoint Foundation","Web Analytics Services"
```

This example merges the last hour of log data from the  `SharePoint Foundation` and  `Web Analytics Services` areas. 
  
--------------EXAMPLE 4-----------------
  
```
Merge-SPLogFile -Path "C:\Logs\FarmMergedLog.log" -Overwrite -Level High
```

This example merges the log data of level  `High` or higher. 
  
--------------EXAMPLE 5-----------------
  
```
Merge-SPLogFile -Path "C:\Logs\FarmMergedLog.log" -Overwrite -StartTime "06/09/2008 16:00" - EndTime "06/09/2008 16:15"
```

This example merges the log data for events in a particular time range, which is culture-specific to the United States.
  
--------------EXAMPLE 6-----------------
  
```
Merge-SPLogFile -Path "C:\Logs\FarmMergedLog.log" -Overwrite -Message "*permission changed*"
```

This example merges the log data for events with  `permission changed` in the message text. 
  
--------------EXAMPLE 7-----------------
  
```
Merge-SPLogFile -Overwrite -Path d:\1.log -ContextFilter "name=timer job*" -Area "*search*"
```

This example merges the log data for all search timer jobs.
  
--------------EXAMPLE 8-----------------
  
```
Merge-SPLogFile -Overwrite -Path d:\2.log -ContextFilter "user=contoso?joeuser"
```

This example shows how to merge the log data for all user names that have a contoso\joeuser or Contoso/joeuser format.
  
## See also

#### 

[New-SPLogFile](new-splogfile.md)

