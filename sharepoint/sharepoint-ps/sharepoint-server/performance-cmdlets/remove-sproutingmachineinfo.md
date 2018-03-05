---
title: "Remove-SPRoutingMachineInfo"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b2176c45-fcb3-4a8f-bac3-5a4da509ea5d

description: "Removes an external routing target."
---

# Remove-SPRoutingMachineInfo

Removes an external routing target.
  
```
Remove-SPRoutingMachineInfo [-Identity] <SPRoutingMachineInfoPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Remove-SPRoutingMachineInfo** cmdlet to remove an external routing target by using the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachineInfoPipeBind  <br/> |Specifies the computer object that Request Manager will remove.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachineInfoPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

----------EXAMPLE-------
  
```
$web=Get-SPWebApplication -Identity <URL of web application>
```

```
$rm=Get-SPRequestManagementSettings -Identity $web
```

```
$M=Get-SPRoutingMachineInfo -RequestManagementSettings $rm -Name <MachineName>
```

```
Remove-SPRoutingMachineInfo -Identity $M
```

This example removes a routing target for a specified identity.
  
## See also

#### 

[Add-SPRoutingMachineInfo](add-sproutingmachineinfo.md)
  
[Get-SPRoutingMachineInfo](get-sproutingmachineinfo.md)
  
[Set-SPRoutingMachineInfo](set-sproutingmachineinfo.md)

