---
title: "Merge-SPUsageLog"
ms.author: kirks
author: Techwriter40
ms.date: 11/7/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5f019815-a0c2-49b1-b0e2-19b63ad5538c

description: "Returns records from usage log files."
---

# Merge-SPUsageLog

Returns records from usage log files.
  
```
Merge-SPUsageLog -Identity <SPUsageDefinitionPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-DiagnosticLogPath <String>] [-EndTime <DateTime>] [-OverWrite <SwitchParameter>] [-Servers <String[]>] [-StartTime <DateTime>]

```

## Example

-------------------EXAMPLE 1-------------------
  
```
Merge-SPUsageLog -Identity "Administrative Actions"
```

This example merges the last hour of log data for "Administrative Actions" usage provider from all farm computers.
  
-------------------EXAMPLE 2-------------------
  
```
Merge-SPUsageLog -Identity "Administrative Actions" -Servers "A-0606","A-0505" -StartTime "06/09/2008 16:00"
```

This example merges the log entries for the "Administrative Actions" usage provider from "06/09/2008 16:00" till now from servers named "A-0606" and "A-0505".
  
-------------------EXAMPLE 3-------------------
  
```
Get-SPUsageDefinition -Identity "Administrative Actions" | Merge-SPUsagelog  -StartTime "08/11/2016 3:50 AM" | Select User, ActionName, Timestamp | Sort Timestamp 

```

This example retrieves Administrative Actions logs starting from Aug 11th, and then selects the following fields to display: **User**, **ActionName**, and **TimeStamp**. The results are sorted by TimeStamp. 
  
This example uses the Windows PowerShell pipeline. For more information about how to use the pipeline, see [about_Pipelines](https://technet.microsoft.com/en-us/library/hh847902.aspx)
  
## Detailed Description

The **Merge-SPUsageLog** cmdlet returns records from usage log files on each farm server that match the criteria, and writes the results to pipeline. 
  
The command gathers, filters, and aggregates logs base on user specified criteria, we recommend that you filter by using the **StartTime** and **EndTime** parameters to optimize performance of this cmdlet. 
  
The output of the **Merge-SPUsageLog** cmdlet will look like this: 
  
|||
|:-----|:-----|
|Parent Type :  <br/> |Microsoft.SharePoint.Administration.SPAdministrationActionProvider  <br/> |
|ActionName :  <br/> |Administration.SiteCollection.User.Add  <br/> |
|TargetName :  <br/> |Domain\User  <br/> |
|Details :  <br/> |{"WebUrl":"http://server:8080","Email":"user@contoso.com","UserCollectionType":"UCT_GroupUsers","Group":"Farm Administrators"}  <br/> |
|FarmId :  <br/> |3ce23179-add1-4330-bb4f-dedc4c193d2f  <br/> |
|User :  <br/> |Domain\AdministratorAccount  <br/> |
|SiteSubscriptionId :  <br/> |00000000-0000-0000-0000-000000000000  <br/> |
|Timestamp :  <br/> |6/14/2016 8:28:07 PM  <br/> |
|TimestampUtc :  <br/> |6/15/2016 3:28:07 AM  <br/> |
|ParentTypeGuid :  <br/> |0e82641e-4c17-416d-ad88-6c1a37c0f567  <br/> |
|CorrelationId :  <br/> |6e44869d-034b-f0d2-0000-006fa8b990c3  <br/> |
|MachineName :  <br/> |Server  <br/> |
|ParentInstanceName :  <br/> ||
   
You should at least specify a usage type. For information on valid usage types, see [Get-SPUsageDefinition](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/service-application-cmdlets/get-spusagedefinition.md).
  
> [!NOTE]
> This cmdlet was first available in the November 2016 Public Update for SharePoint Server 2016 (Feature Pack 1). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUsageDefinitionPipeBind  <br/> |Specifies the name of usage log file.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _DiagnosticLogPath_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the file to write diagnostic information to. A relative path is supported.  <br/> |
| _EndTime_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the end time of the log entries returned.  <br/> The type must be a valid DateTime format that is culture-specific to the administrative language, that is, 2/16/2007 12:15:12 for English-US.  <br/> The default value is the current time.  <br/> If you want to specify UTC time, you must add a "Z" to the end of the parameter. For example, "2016-06-15 03:29:18.199 Z". If the "Z" is not specify, local computer time will be displayed instead of UTC.  <br/> |
| _OverWrite_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Overwrites the diagnostic log file if it already exists at the specified path.  <br/> |
| _Servers_ <br/> |Optional  <br/> |System.String[]  <br/> |The server address or addresses to filter on.  <br/> To obtain a list of valid addresses in the farm use  `Get-SPServer | Select Address`.  <br/> |
| _StartTime_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the start time of the log entries returned.  <br/> The type must be a valid DateTime format that is culture-specific to the administrative language, such as "2/16/2007 12:15:12" for English-US.  <br/> The default value is one hour prior to the current time on the local computer.  <br/> If you want to specify UTC time, you must add a "Z" to the end of the parameter. For example, "2016-06-15 03:29:18.199 Z". If the "Z" is not specify, local computer time will be displayed instead of UTC.  <br/> |
   

