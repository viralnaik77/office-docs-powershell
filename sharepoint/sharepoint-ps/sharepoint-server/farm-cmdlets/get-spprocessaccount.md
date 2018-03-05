---
title: "Get-SPProcessAccount"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/4/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4ac70aeb-3dd0-46ec-b578-27b271ef2236

description: "Returns a system account or a managed account."
---

# Get-SPProcessAccount

Returns a system account or a managed account.
  
```
Get-SPProcessAccount [-AssignmentCollection <SPAssignmentCollection>] [-NetworkService <SwitchParameter>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPProcessAccount** cmdlet returns a system account or a managed account and creates the **SPProcessAccountPipeBind** object. All operations that can accept an account can accept the **SPProcessAccountPipeBind** in place of the **SPManagedAccountPipeBind**.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**LocalService** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Returns the LocalService account.  <br/> |
|**LocalSystem** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Returns the LocalSystem account.  <br/> |
|**NetworkService** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Returns the NetworkService account.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**LocalService** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**LocalSystem** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**NetworkService** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Errors

|**Error**|**Description**|
|:-----|:-----|
|||
   
## Exceptions

|**Exceptions**|**Description**|
|:-----|:-----|
|||
   
## Example

------------------EXAMPLE 1-----------------------
  
```
Get-SPProcessAccount -NetworkService
```

This example creates the **SPProcessAccountPipeBind** type by using the  `NetworkService` account. 
  
------------------EXAMPLE 2-----------------------
  
```
Get-SPProcessAccount -NetworkService | New-SPServiceApplicationPool -Account $_
```

This example creates an  `SPServiceApplicationPool` account by using the  `NetworkService` account returned by the  `Get-SPProcessAccount` cmdlet. 
  

