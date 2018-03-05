---
title: "Add-SPRoutingMachineInfo"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c72761cb-712d-463e-94b4-9b68fad776d3

description: "Adds a new routing target to the farm."
---

# Add-SPRoutingMachineInfo

Adds a new routing target to the farm.
  
```
Add-SPRoutingMachineInfo -Name <String> -RequestManagementSettings <SPRequestManagementSettingsPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Availability <Available | Unavailable>] [-OutgoingPort <Int32>] [-OutgoingScheme <SameAsIncoming | Http | Https>] [-StaticWeight <Double>]

```

## Example

-------------EXAMPLE--------------
  
```
$web=Get-SPWebApplication -Identity <URL of web application>
```

```
$rm=Get-SPRequestManagementSettings -Identity $web
```

```
Add-SPRoutingMachineInfo -RequestManagementSettings $rm -Name <MachineName> -Availability Available
```

```

```

This example adds a routing target for a specified identity to the farm.
  
## Detailed Description

Use the **Add-SPRoutingMachineInfo** cmdlet to add a new routing target to the farm by using the **RequestManagementSettings** and **Name** parameters. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the computer to add to the route.  <br/> |
| _RequestManagementSettings_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> |Specifies the name of the request management settings object to add to the routing target.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Availability_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPRoutingMachineAvailability  <br/> |Specifies whether or not the added computer will be available for routing.  <br/> The valid values are:  <br/> --Available  <br/> --Unavailable  <br/> |
| _OutgoingPort_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the port used by Request Manager to make an outgoing connection.  <br/> |
| _OutgoingScheme_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPRoutingOutgoingScheme  <br/> |Determines the Http scheme of outgoing connections.  <br/> The valid values are:  <br/> --SameAsIncoming  <br/> --Http  <br/> --Https  <br/> |
| _StaticWeight_ <br/> |Optional  <br/> |System.Double  <br/> |Specifies the static weight of a computer routing that is used by Request Manager. If the static weight is higher, more requests will be routed to the computer.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**RequestManagementSettings** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Availability** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**OutgoingPort** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**OutgoingScheme** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**StaticWeight** <br/> |Optional  <br/> |System.Nullable  <br/> ||
   
## See also

#### 

[Get-SPRoutingMachineInfo](get-sproutingmachineinfo.md)
  
[Remove-SPRoutingMachineInfo](remove-sproutingmachineinfo.md)
  
[Set-SPRoutingMachineInfo](set-sproutingmachineinfo.md)

