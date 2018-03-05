---
title: "Get-SPManagedAccount"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ad7377ab-25bf-49b8-b619-bc70ea122a3c

description: "Retrieves accounts registered in the configuration database."
---

# Get-SPManagedAccount

Retrieves accounts registered in the configuration database.
  
```
Get-SPManagedAccount [[-Identity] <SPManagedAccountPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Service <SPServicePipeBind>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPManagedAccount** cmdlet returns the managed accounts that match the given scope. The scope can be any one of the following values: **Web application**, **service**, or **server**. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPManagedAccountPipeBind  <br/> |Specifies the full name or partial name of the managed accounts to retrieve.  <br/> The type must be a valid account name, in the form Domain\User, or a GUID, in the form 1234-3456-09876.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Server** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServerPipeBind  <br/> |Specifies the scope to a server.  <br/> |
|**Service** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServicePipeBind  <br/> |Specifies the scope to a service.  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the scope to a Web application.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPManagedAccountPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Server** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServerPipeBind  <br/> ||
|**Service** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServicePipeBind  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPManagedAccount
```

This example displays all the managed accounts in the farm.
  
## See also

#### 

[New-SPManagedAccount](new-spmanagedaccount.md)
  
[Set-SPManagedAccount](set-spmanagedaccount.md)
  
[Remove-SPManagedAccount](remove-spmanagedaccount.md)

