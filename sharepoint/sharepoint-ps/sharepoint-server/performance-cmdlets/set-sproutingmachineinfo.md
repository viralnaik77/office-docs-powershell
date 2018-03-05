---
title: "Set-SPRoutingMachineInfo"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7fd919f3-8a3d-4f29-8266-9f8a7838588c

description: "Sets routing target properties."
---

# Set-SPRoutingMachineInfo

Sets routing target properties.
  
```
Set-SPRoutingMachineInfo -Identity <SPRoutingMachineInfoPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Availability <Available | Unavailable>] [-ClearOutgoingPort <SwitchParameter>] [-OutgoingPort <Int32>] [-OutgoingScheme <SameAsIncoming | Http | Https>] [-StaticWeight <Double>]

```

## Example

------------EXAMPLE----------
  
```
$web=Get-SPWebApplication -Identity <URL of web application>
```

```
$rm=Get-SPRequestManagementSettings -Identity $web
```

```
$m=Get-SPRoutingMachineInfo -RequestManagementSettings $rm -Name <MachineName>
```

```
Set-SPRoutingMachineInfo -Identity $m -Availability Unavailable
```

This example sets the "Availability" routing target property to Unavailable for a specified identity.
  
## Detailed Description

Use the **Set-SPRoutingMachineInfo** cmdlet to set routing target properties by using the **Identity** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachineInfoPipeBind  <br/> |Specifies the name of the request management settings object to set.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Availability_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPRoutingMachineAvailability  <br/> |Specifies whether or not the specified computer will be available for routing.  <br/> The valid values are:  <br/> --Available  <br/> --Unavailable  <br/> |
| _ClearOutgoingPort_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Clears the outgoing port if it is set.  <br/> |
| _OutgoingPort_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the listening port for the computer that Request Management will use to communicate with.  <br/> |
| _OutgoingScheme_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPRoutingOutgoingScheme  <br/> |Determines the schema of outgoing connections.  <br/> The valid values are:  <br/> --SameAsIncoming  <br/> --Http  <br/> --Https  <br/> |
| _StaticWeight_ <br/> |Optional  <br/> |System.Double  <br/> |Specifies whether the static weight of a computer routing is used by Request Manager. If the static weight is higher, more requests will be routed to the computer.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRoutingMachineInfoPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Availability** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**ClearOutgoingPort** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**OutgoingPort** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**OutgoingScheme** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**StaticWeight** <br/> |Optional  <br/> |System.Nullable  <br/> ||
   
## See also

#### 

[Add-SPRoutingMachineInfo](add-sproutingmachineinfo.md)
  
[Get-SPRoutingMachineInfo](get-sproutingmachineinfo.md)
  
[Remove-SPRoutingMachineInfo](remove-sproutingmachineinfo.md)

