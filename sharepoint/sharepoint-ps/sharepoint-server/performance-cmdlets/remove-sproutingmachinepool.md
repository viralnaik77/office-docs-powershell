---
title: "Remove-SPRoutingMachinePool"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 053eee92-2bdd-4d48-baf8-379db33b5fcf

description: "Removes a routing pool from Request Manager."
---

# Remove-SPRoutingMachinePool

Removes a routing pool from Request Manager.
  
```
Remove-SPRoutingMachinePool [-Identity] <SPRoutingMachinePoolPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Remove-SPRoutingMachinePool** cmdlet to remove a routing pool from the Request Manager object by using the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachinePoolPipeBind  <br/> |Specifies the Request Manager object to remove.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachinePoolPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-------------EXAMPLE----------
  
```
$web=Get-SPWebApplication -Identity <URL of web application>
```

```
$rm=Get-SPRequestManagementSettings -Identity $web
```

```
$pool=Get-SPRoutingMachinePool -RequestManagementSettings $rm
```

```
Remove-SPRoutingMachinePool -Identity $pool
```

This example removes a routing pool for the specified identity by using the **$pool** variable. 
  
## See also

#### 

[Add-SPRoutingMachinePool](add-sproutingmachinepool.md)
  
[Get-SPRoutingMachinePool](get-sproutingmachinepool.md)
  
[Set-SPRoutingMachinePool](set-sproutingmachinepool.md)

