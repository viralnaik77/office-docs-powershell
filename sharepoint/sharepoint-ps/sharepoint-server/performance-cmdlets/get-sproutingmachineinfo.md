---
title: "Get-SPRoutingMachineInfo"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e20c9708-1eb9-4a60-9e80-6d9b132c17e8

description: "Returns all the routing targets."
---

# Get-SPRoutingMachineInfo

Returns all the routing targets.
  
```
Get-SPRoutingMachineInfo -RequestManagementSettings <SPRequestManagementSettingsPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Availability <Available | Unavailable>] [-Name <String>]

```

## Example

------------EXAMPLE------------
  
```
$web=Get-SPWebApplication -Identity <URL of web application>
```

```
$rm=Get-SPRequestManagementSettings -Identity $web
```

```
Get-SPRoutingMachineInfo -RequestManagementSettings $rm
```

This example returns a routing target for a specified identity.
  
## Detailed Description

Use the **Get-SPRoutingMachineInfo** cmdlet to return all the routing targets that are being used by the Request Manager object. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _RequestManagementSettings_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> |Specifies the name of the request management settings object to return.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Availability_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPRoutingMachineAvailability  <br/> |Specifies whether or not the specified computer will be available for routing. If no value is specified, all computers are returned.  <br/> The values for this parameter are filtered based on availability.  <br/> The valid values are:  <br/> --Available  <br/> --Unavailable  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the computer for which you want to return routing information.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RequestManagementSettings** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Availability** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
   
## See also

#### 

[Add-SPRoutingMachineInfo](add-sproutingmachineinfo.md)
  
[Remove-SPRoutingMachineInfo](remove-sproutingmachineinfo.md)
  
[Set-SPRoutingMachineInfo](set-sproutingmachineinfo.md)

