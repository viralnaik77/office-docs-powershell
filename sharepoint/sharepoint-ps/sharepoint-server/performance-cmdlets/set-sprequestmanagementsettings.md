---
title: "Set-SPRequestManagementSettings"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 6/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9c4d9bd-b693-4933-a3f5-011691693abe

description: "Sets Request Manager properties."
---

# Set-SPRequestManagementSettings

Sets Request Manager properties.
  
```
Set-SPRequestManagementSettings -Identity <SPRequestManagementSettingsPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-RoutingEnabled <SwitchParameter>] [-RoutingScheme <Default | StaticMachineWeight | HealthBased>] [-ThrottlingEnabled <SwitchParameter>]

```

## Detailed Description

Use the **Set-SPRequestManagementSettings** cmdlet to set properties for the Request Manager. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> |Specifies the Request Manager object for which settings will be applied.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _RoutingEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether routing is enabled or disabled for the Request Manager object.  <br/> |
| _RoutingScheme_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPRoutingScheme  <br/> |Specifies the routing scheme.  <br/> The value is one of the following:  <br/> -- **Default** - Performs random selection.  <br/> -- **StaticMachineWeight** - Uses Static weight of target.  <br/> -- **HealthBased** - Considers health score of machine.  <br/> |
| _ThrottlingEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether throttling is enabled or disabled for the Request Manager object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPRequestManagementSettingsPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**RoutingEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**RoutingScheme** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**ThrottlingEnabled** <br/> |Optional  <br/> |System.Nullable  <br/> ||
   
## See also

#### 

[Get-SPRequestManagementSettings](get-sprequestmanagementsettings.md)
  
[New-SPRequestManagementRuleCriteria](new-sprequestmanagementrulecriteria.md)

