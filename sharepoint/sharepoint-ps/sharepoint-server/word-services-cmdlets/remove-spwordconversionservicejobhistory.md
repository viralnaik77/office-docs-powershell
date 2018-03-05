---
title: "Remove-SPWordConversionServiceJobHistory"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4ed215c-cb20-4171-9013-2cc243e106d2

description: "Removes entries from the Word Automation Services job history database."
---

# Remove-SPWordConversionServiceJobHistory

Removes entries from the Word Automation Services job history database.
  
```
Remove-SPWordConversionServiceJobHistory -Identity <WordServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-BeforeDate <DateTime>] [-Confirm [<SwitchParameter>]] [-IncludeActiveJobs <SwitchParameter>] [-JobId <Guid>] [-SubscriptionId <Guid>] [-WhatIf [<SwitchParameter>]]

```

## Example

---------------------EXAMPLE 1------------------------ 
  
```
Get-SPServiceApplication -Name TestWordServer | Remove-SPWordConversionServiceJobHistory -BeforeDate 1/1/2009
```

This example deletes all the items in the database before  `1/1/2009`.
  
---------------------EXAMPLE 2------------------------ 
  
```
Get-SPServiceApplication -Name TestWordServer | Remove-SPWordConversionServiceJobHistory -JobId 00000000-0000-0112-08FF-63927635FEF1 -IncludeActiveJobs
```

This example deletes the job with the specified ID, even if it is still processing.
  
## Detailed Description

The **Remove-SPWordConversionServiceJobHistory** cmdlet removes entries from the Word Automation Services job history database. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Word.Server.Powershell.WordServiceApplicationPipeBind  <br/> |Specifies the Word Automation Services application to be processed.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Word Automation Services application (for example, WordSvcApp1); or an instance of a valid **SPServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _BeforeDate_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies that only jobs started before this date are to be removed.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _IncludeActiveJobs_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that jobs that contain active conversions can be removed. By default, jobs that have active conversions are not removed.  <br/> |
| _JobId_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that only the job with the specified ID is to be removed.  <br/> |
| _SubscriptionId_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that only jobs corresponding to this subscription ID are to be removed.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**BeforeDate** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**IncludeActiveJobs** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**JobId** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SubscriptionId** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

