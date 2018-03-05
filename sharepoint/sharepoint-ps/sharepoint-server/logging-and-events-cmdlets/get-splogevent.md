---
title: "Get-SPLogEvent"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 25fd4b29-f4d3-43bb-bf2b-57d395882046

description: "Returns results from a Unified Logging Service (ULS) trace log."
---

# Get-SPLogEvent

Returns results from a Unified Logging Service (ULS) trace log.
  
```
Get-SPLogEvent [-AssignmentCollection <SPAssignmentCollection>] [-AsString <SwitchParameter>] [-ContextKey <String[]>] [-Directory <String>] [-EndTime <DateTime>] [-MinimumLevel <String>] [-StartTime <DateTime>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPLogEvent** cmdlet returns records from a ULS trace log file that match the criteria. If no parameters are specified, all records from all log files are returned. Use the **StartTime** and **EndTime** parameters to filter on a time range. The use of these parameters is recommended to optimize performance of this cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentColletion  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**AsString** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Returns each record as a separate string  <br/> |
|**ContextKey** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies that context data should be added to the results for the specified Context Keys, for example: -ContextKey @("UserName", "SiteName").  <br/> |
|**Directory** <br/> |Optional  <br/> |System.String  <br/> |Lists log files from an alternate directory (any directory other than the configured LogLocation directory).  <br/> |
|**MinimumLevel** <br/> |Optional  <br/> |System.String  <br/> |Returns records at or above the specified level. The valid values are (in order of severity): **Information**, **Medium**, **High**, **Verbose**, **VerboseEx**, **Monitorable**, **Warning**, **Error**, **Critical**, or **Unassigned**.  <br/> |
|**EndTime** <br/> |Optional  <br/> |System.DateTime  <br/> |The type must be a valid DateTime format that is culture-specific to the administrative language, such as 2/16/2007 12:15:12 for English-US.  <br/> |
|**File** <br/> |Optional  <br/> |System.String  <br/> |Specifies a specific file to query records from.  <br/> |
|**StartTime** <br/> |Optional  <br/> |System.DateTime  <br/> |The type must be a valid DateTime format that is culture-specific to the administrative language, such as 2/16/2007 12:15:12 for English-US.  <br/> |
   
## Example

--------------EXAMPLE 1-----------------
  
```
Get-SPLogEvent -MinimumLevel "Warning"
```

This example returns all log entries equal to or more severe than Warning from the default log directory.
  
--------------EXAMPLE 2-----------------
  
```
Get-SPLogEvent -Directory "C:\Logs" | Where-Object {$_.Level -eq "Warning"}
```

This example returns all warning entries from log files in the C:\Logs directory.
  
--------------EXAMPLE 3-----------------
  
```
Get-SPLogEvent -StartTime "12/04/2007 17:00" -EndTime "12/04/2007 18:00"
```

This example returns error entries that occurred during a particular time range, which is culture-specific to the United States.
  
--------------EXAMPLE 4-----------------
  
```
Get-SPLogEvent -ContextKey @("UserName" ,"SiteName")
```

This example returns the contents of the most recent log file and adds the specified context key data.
  
--------------EXAMPLE 5-----------------
  
```
Get-SPLogEvent | Where-Object {$_.Level -eq "Error" -and {$_.Area -eq "SharePoint Foundation "}
```

This example returns all error entries related to SharePoint Foundation.
  
--------------EXAMPLE 6-----------------
  
```
Get-SPLogEvent -ContextKey @("Name") | %{$_.ToString() + "'t" + $_.Context["Name"]}
```

This example returns the contents of the log file and adds context data.
  
## See also

#### 

[New-SPLogFile](new-splogfile.md)
  
[Get-SPLogLevel](get-sploglevel.md)

