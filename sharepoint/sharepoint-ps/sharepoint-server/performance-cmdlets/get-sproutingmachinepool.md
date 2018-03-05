---
title: "Get-SPRoutingMachinePool"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b2116a73-174c-4bdd-98de-63639794e75f

description: "Returns all available routing pools."
---

# Get-SPRoutingMachinePool

Returns all available routing pools.
  
```
Get-SPRoutingMachinePool [-RequestManagementSettings] <SPRequestManagementSettingsPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Name <String>]
```

## Detailed Description

Use the **Get-SPRoutingMachinePool** cmdlet to return all available routing pools by using the **RequestManagementSettings** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RequestManagementSettings** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> |Specifies the name of the request management settings object to return.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the machine pool to return.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RequestManagementSettings** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

--------------EXAMPLE---------
  
```
$web=Get-SPWebApplication -Identity <URL of web application>
```

```
$rm=Get-SPRequestManagementSettings -Identity $web
```

```
Get-SPRoutingMachinePool -RequestManagementSettings $rm
```

This example returns a routing pool for the specified identity.
  
## See also

#### 

[Add-SPRoutingMachinePool](add-sproutingmachinepool.md)
  
[Remove-SPRoutingMachinePool](remove-sproutingmachinepool.md)
  
[Set-SPRoutingMachinePool](set-sproutingmachinepool.md)

