---
title: "New-SPPerformancePointServiceApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/28/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f65f3b36-6495-4738-86f3-c9024293f06c

description: "Creates a new service application for the PerformancePoint Service."
---

# New-SPPerformancePointServiceApplication

Creates a new service application for the PerformancePoint Service.
  
```
New-SPPerformancePointServiceApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> -Name <String> [-AnalyticQueryCellMax <Int32>] [-AnalyticQueryLoggingEnabled <$true | $false>] [-AnalyticResultCacheMinimumHitCount <Int32>] [-ApplicationCacheEnabled <$true | $false>] [-ApplicationCacheMinimumHitCount <Int32>] [-ApplicationProxyCacheEnabled <$true | $false>] [-AssignmentCollection <SPAssignmentCollection>] [-CommentsDisabled <$true | $false>] [-CommentsScorecardMax <Int32>] [-Confirm [<SwitchParameter>]] [-DatabaseFailoverServer <String>] [-DatabaseName <String>] [-DatabaseServer <String>] [-DatabaseSQLAuthenticationCredential <PSCredential>] [-DataSourceQueryTimeoutSeconds <Int32>] [-DataSourceUnattendedServiceAccountTargetApplication <String>] [-DecompositionTreeMaximum <Int32>] [-ElementCacheSeconds <Int32>] [-FilterRememberUserSelectionsDays <Int32>] [-FilterSearchResultsMax <Int32>] [-FilterTreeMembersMax <Int32>] [-IndicatorImageCacheSeconds <Int32>] [-MSMQEnabled <$true | $false>] [-MSMQName <String>] [-SelectMeasureMaximum <Int32>] [-SessionHistoryHours <Int32>] [-ShowDetailsInitialRows <Int32>] [-ShowDetailsMaxRows <Int32>] [-ShowDetailsMaxRowsDisabled <$true | $false>] [-TrustedContentLocationsRestricted <$true | $false>] [-TrustedDataSourceLocationsRestricted <$true | $false>] [-UseEffectiveUserName <$true | $false>] [-WhatIf [<SwitchParameter>]]

```

## Example

-----------------EXAMPLE------------------------
  
```
New-SPPerformancePointServiceApplication -Name PPS_Application_01 -ApplicationPool PPS_Application_Pool_01
```

This example creates a new PerformancePoint Service application named  `PPSApp_01` and sets it to run under an application pool named  `PPS_Application_Pool_01`.
  
## Detailed Description

The **New-SPPerformancePointServiceApplication** cmdlet creates a new PerformancePoint Service on the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ApplicationPool_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the existing IIS application pool to run the Web service in for the service application.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPoolName1); or an instance of a valid **IISWebServiceApplicationPool** object.  <br/> |
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new PerformancePoint Service application.  <br/> The type must be a valid name of a PerformancePoint Service application; for example, PerfPointApp1.  <br/> |
| _AnalyticQueryCellMax_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of returned cells in an analytic grid.  <br/> A valid integer value from 1 through 1,000,000,000. The default value is **100,000**.  <br/> |
| _AnalyticQueryLoggingEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Turns on verbose logging of query events.  <br/> The type must be one of the following: True or False. The default value is **False**.  <br/> |
| _AnalyticResultCacheMinimumHitCount_ <br/> |Optional  <br/> |System.Int32  <br/> |The minimum number of times an analytic report needs to be accessed before caching starts happening.  <br/> The default value is 0.  <br/> |
| _ApplicationCacheEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the rendered output cache on the application server is on (True) or off (False). The default value is **True**.  <br/> |
| _ApplicationCacheMinimumHitCount_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the minimum number of times rendered output must be requested before it is added to cache. The default value is **2**.  <br/> |
| _ApplicationProxyCacheEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies rendered output cache on the front end Web server. The default value is **True**.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CommentsDisabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that users can add comments to scorecard cells.  <br/> The type must be one of the following: true or false.  <br/> |
| _CommentsScorecardMax_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of comments that can be added to a scorecard. The default value is **1000**.  <br/> The type must be an integer value from 1 through 1,000,000.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseFailoverServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database server that contains the PerformancePoint Services database that must be mirrored.  <br/> This parameter was introduced in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1).  <br/> |
| _DatabaseName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the PerformancePoint Services database that will be created when the service application is provisioned.  <br/> This parameter was introduced in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1).  <br/> |
| _DatabaseServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the database server where the PerformancePoint Services database will be created. This should be the same server name that is used for the SharePoint content and configuration databases.  <br/> The value may be written as **SQL instance\server** if it is not referring to the default instance.  <br/> This parameter was introduced in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1).  <br/> |
| _DatabaseSQLAuthenticationCredential_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Determines whether to use Windows authentication or SQL Server authentication when connecting to a PerformancePoint Services database.  <br/> This parameter was introduced in SharePoint Server 2010 with Service Pack 1 (SP1) and SharePoint Foundation 2010 with Service Pack 1 (SP1).  <br/> |
| _DataSourceQueryTimeoutSeconds_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the time, in seconds, before a data source query times out. The default value is **300**.  <br/> The type must be an integer value in the range of 1 to 36,000.  <br/> |
| _DataSourceUnattendedServiceAccountTargetApplication_ <br/> |Optional  <br/> |System.String  <br/> |The name of the Secure Store Application that will be used by default to access data sources.  <br/> |
| _DecompositionTreeMaximum_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of items (per level) returned to the decomposition tree visualization.  <br/> A valid integer value from 1 through 1,000,000. The default value is **25**.  <br/> |
| _ElementCacheSeconds_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the first class object cache expiration time. The default value is **15**.  <br/> |
| _FilterRememberUserSelectionsDays_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of days that user filter selections are remembered. The default value is **90**.  <br/> The type must be an integer value from 1 through 10,000.  <br/> |
| _FilterSearchResultsMax_ <br/> |Optional  <br/> |System.Int32  <br/> |The maximum number of items to return on a Dashboard when viewing a filter.  <br/> The default value is **5000**.  <br/> |
| _FilterTreeMembersMax_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of records to show in filter treeview control. The default value is **500**.  <br/> The type must be an integer value from 1 through 100,000.  <br/> |
| _IndicatorImageCacheSeconds_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the time, in seconds, that key performance indicator (KPI) icons are cached. The default value is **10**.  <br/> The type must be an integer value from 1 through 3,600.  <br/> |
| _MSMQEnabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that notifications are sent to Microsoft Message Queuing (MSMQ) on content change.  <br/> The type must be one of the following: true or false. The default value is **False**.  <br/> |
| _MSMQName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the queue. The queue name can contain a maximum of 380 characters, and cannot contain the following characters: CR (ASCII 13), LF (ASCII 10), backslash (\), plus sign (+, comma (,), or quotation marks ("") .  <br/> The type must be a valid MSMQ name; for example, MessageQueue1.  <br/> |
| _SelectMeasureMaximum_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of measures to show in a dashboard Select Measure control. The default value is **1000**.  <br/> The type must be an integer value from 1 through 1,000,000.  <br/> |
| _SessionHistoryHours_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of hours between clearing expired user navigation history. The default value is **2**.  <br/> The type must be an integer value from 1 through 48.  <br/> |
| _ShowDetailsInitialRows_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the initial number of rows to retrieve for show details. The default value is 1,000.  <br/> The type must be an integer value from 1 through 100,000.  <br/> |
| _ShowDetailsMaxRows_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of rows to retrieve for show details.  <br/> The type must be an integer value from 1 through 1,000,000. The default value is 10,000.  <br/> |
| _ShowDetailsMaxRowsDisabled_ <br/> |Optional  <br/> |System.Boolean  <br/> |Turns off the **ShowDetailsInitialRows** setting. If set to True, Analysis Services controls limit.  <br/> The type must be one of the following: **True** or **False**. The default value is **False**.  <br/> |
| _TrustedContentLocationsRestricted_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that only specified locations are trusted. The default setting is false (trust all content locations).  <br/> The type must be one of the following: **True** or **False**. The default value is **False**.  <br/> |
| _TrustedDataSourceLocationsRestricted_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies that only specified locations are trusted. The default setting is false (trust all data source locations).  <br/> The type must be one of the following: **True** or **False**. The default value is **False**.  <br/> |
| _UseEffectiveUserName_ <br/> |Optional  <br/> |System.Boolean  <br/> |Enables the use of the Analysis Services Effective User Name feature.  <br/> The type must be one of the following: **True** or **False**. The default value is **False**.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPPerformancePointServiceApplication](get-spperformancepointserviceapplication.md)
  
[Remove-SPPerformancePointServiceApplication](remove-spperformancepointserviceapplication.md)
  
[Set-SPPerformancePointServiceApplication](set-spperformancepointserviceapplication.md)

