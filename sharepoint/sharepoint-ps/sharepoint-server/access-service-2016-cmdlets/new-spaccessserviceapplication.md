---
title: "New-SPAccessServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3ebea335-3e0c-44af-bf80-6f6f19668608

description: "Creates a new instance of an Access Services application in SharePoint Server 2016."
---

# New-SPAccessServiceApplication

Creates a new instance of an Access Services application in SharePoint Server 2016.
  
```
New-SPAccessServiceApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-ApplicationLogSizeMax <Int32>] [-AssignmentCollection <SPAssignmentCollection>] [-CacheTimeout <Int32>] [-ColumnsMax <Int32>] [-Confirm [<SwitchParameter>]] [-Default <SwitchParameter>] [-Name <String>] [-NonRemotableQueriesAllowed <SwitchParameter>] [-OrderByMax <Int32>] [-OuterJoinsAllowed <SwitchParameter>] [-OutputCalculatedColumnsMax <Int32>] [-PrivateBytesMax <Int32>] [-RecordsInTableMax <Int32>] [-RequestDurationMax <Int32>] [-RowsMax <Int32>] [-SessionMemoryMax <Int32>] [-SessionsPerAnonymousUserMax <Int32>] [-SessionsPerUserMax <Int32>] [-SourcesMax <Int32>] [-TemplateSizeMax <Int32>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPAccessServiceApplication** cmdlet creates a new instance of an Access Services application in SharePoint Server 2016. After you create a new Access Services application, use the **Set-SPAccessServiceApplication** cmdlet to modify its global settings. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name of the Access Services application to create. The name can contain a maximum of 128 characters and can contain the comma (,), equal sign (=), or colon (:) characters provided they are enclosed in quotation marks.  <br/> The type must be a valid name of an Access Services application; for example, AccessSrvApp1.  <br/> |
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the existing Internet Information Services (IIS) application pool to run the Web service in for the new Access Services application.  <br/> The type must be a valid instance of a **SPIisWebServiceApplicationPool** object.  <br/> |
|**ApplicationLogMaxSize** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of records for an Access Services Application Log list. Valid valies: -1 to maxint. 0 means none are allowed. The default value is 3000.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CacheTimeout** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of seconds that a data cache will remain active on Access Services with no user activity. Valid values include: **-1**, cache never times out; 1 to 2073600, cache remains active from 1 second to 24 days.  <br/> The type must be the integers -1, or an integer in the range of 1 to 2073600 (24 days). The default value is **300**.  <br/> |
|**ColumnsMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of columns that a list involved in a query can contain, or that the output of the query can contain. The default value is **30**.  <br/> The type must be an integer in the range of 1 to 255  <br/> |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Default** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application is associated with Web applications by adding this service application's proxy to the farm's default proxy list.  <br/> |
|**NonRemotableQueriesAllowed** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that queries that cannot be remoted to the database tier can run.  <br/> |
|**OrderByMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of Order By clauses in the query. The default value is **4**.  <br/> The type must be an integer in the range of 1 to 8.  <br/> |
|**OuterJoinsAllowed** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that left and right outer joins are supported. Inner joins are always supported.  <br/> |
|**OutputCalculatedColumnsMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of calculated columns that can be included in the output as a part of the query. Calculated columns in the underlying list are not included. The default value is **10**.  <br/> The type must be an integer in the range of 1 to 32.  <br/> |
|**PrivateBytesMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum private bytes in megabytes (MB) that can be used by Access Services. When set to -1, Access Services defaults to 75 percent of physical memory on the machine. Valid values are -1 (no limit), and from 1 to any positive integer.The default value is - **1**.  <br/> |
|**RecordsInTableMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of records allowed for a table in the Access Services application. Valid values include: -1, no limit, and 1 to any positive integer. The default value is **500000**.  <br/> The type must be the integer -1, or an integer in the range of 1 to MaxInt.  <br/> |
|**RequestDurationMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of seconds that a request to perform an operation can use before the request times out. Valid values include: -1, no limit, 1 to 2073600, cache remains active 1 second to 24 days. The default value is **30**.  <br/> The type must be the integer -1, or an integer in the range of 1 to 2073600 (24 days)  <br/> |
|**RowsMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of rows that a list involved in a query can have, or that the output of the query can have. The default value is **50000**.  <br/> The type must be an integer in the range of 1 to 200000.  <br/> |
|**SessionMemoryMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum allowable size, in megabytes, of an individual session. Valid values include 0, disable property, and 1 to 4095. The default value is **64**.  <br/> The type must be the integer 0, or an integer in the range of 1 to 4095.  <br/> |
|**SessionsPerAnonymousUserMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of sessions allowed per user. If this maximum is reached, the oldest session will be deleted when a new session is started. Valid values include: -1, no limit, and 1 to any positive integer. The default value is **10**.  <br/> The type must be the integer -1, or an integer in the range of 1 to MaxInt.  <br/> |
|**SessionsPerUserMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of sessions allowed per user. If this maximum is reached, the oldest session will be deleted when a new session is started. Valid values include: -1, no limit, and 1 to any positive integer. The default value is **10**.  <br/> The type must be the integer -1, or an integer in the range of 1 to MaxInt.  <br/> |
|**SourcesMax** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of lists that can be used as input to a query at one time. The default value is **8**.  <br/> The type must be an integer in the range of 1 to 20.  <br/> |
|**TemplateSizeMax** <br/> |Optional  <br/> |System.Int32  <br/> |The maximum allowable size in megabytes allowed for Access templates (.accdt file files) uploaded into the solution gallery. Valid values: -1(no limit), from 1 to any positive integer.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ApplicationPool** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**ApplicationLogSizeMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CacheTimeout** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**ColumnsMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Default** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**NonRemotableQueriesAllowed** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**OrderByMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**OuterJoinsAllowed** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**OutputCalculatedColumnsMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**PrivateBytesMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**RecordsInTableMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**RequestDurationMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**RowsMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**SessionMemoryMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**SessionsPerAnonymousUserMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**SessionsPerUserMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**SourcesMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**TemplateSizeMax** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------EXAMPLE 1----------------
  
```
New-SPAccessServiceApplication -Name "MyAccessService" -SPIisWebServiceApplicationPool MyAppPool
```

This example creates a new instance of Access Services named  `MyAccessService` that runs under the application pool named  `MyAppPool`.
  
------------EXAMPLE 2----------------
  
```
New-SPAccessServiceApplication -Name "MyAccessService" -SPIisWebServiceApplicationPool MyAppPool -SessionsPerUserMax 25
```

This example creates a new instance of Access Services named  `MyAccessService` that runs under the application pool named  `MyAppPool`, which allows up to 25 sessions per user on each back end application server machine on which Access Services runs.
  
## See also

#### 

[Set-SPAccessServiceApplication](set-spaccessserviceapplication.md)
  
[Get-SPAccessServiceApplication](get-spaccessserviceapplication.md)

