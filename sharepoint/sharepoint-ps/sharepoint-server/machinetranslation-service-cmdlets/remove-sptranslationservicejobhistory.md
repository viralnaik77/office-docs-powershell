---
title: "Remove-SPTranslationServiceJobHistory"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1ecc2f44-33d2-49a4-aef4-e6b9a3918c85

description: "Removes Machine Translation service jobs."
---

# Remove-SPTranslationServiceJobHistory

Removes Machine Translation service jobs.
  
```
Remove-SPTranslationServiceJobHistory -Identity <TranslationServiceApplicationPipeBind> [-AllPartitions <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-BeforeDate <DateTime>] [-Confirm [<SwitchParameter>]] [-IncludeActiveJobs <SwitchParameter>] [-JobId <Guid>] [-PartitionId <Guid>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE--------------
  
```
Remove-SPTranslationServiceJobHistory TranslationService -BeforeDate 2012/01/31
```

This example removes all jobs completed before 2012/01/31 in the database associated with the Machine Translation Service application named TranslationService. 
  
## Detailed Description

Use the **Remove-SPTranslationServiceJobHistory** cmdlet to remove a machine translation service job from the job history database. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.TranslationServices.Powershell.TranslationServiceApplicationPipeBind  <br/> |Specifies the URL or GUID of the instance of the Machine Translation service to remove.  <br/> The type must be a valid URL, in the form http://server_name or a valid GUID (for example, 12345678-90ab-cdef-1234-567890bcdefgh).  <br/> |
| _AllPartitions_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Removes all the jobs from the database given other parameters.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _BeforeDate_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies all expired jobs before a given date.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _IncludeActiveJobs_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies expired jobs which contain active translations. By default, jobs are not deleted if a translation is active.  <br/> |
| _JobId_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies only a job Id and its items to expire.  <br/> |
| _PartitionId_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies only a partition Id and its items to expire.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.TranslationServices.Powershell.TranslationServiceApplicationPipeBind  <br/> ||
|**AllPartitions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**BeforeDate** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**IncludeActiveJobs** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**JobId** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**PartitionId** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

