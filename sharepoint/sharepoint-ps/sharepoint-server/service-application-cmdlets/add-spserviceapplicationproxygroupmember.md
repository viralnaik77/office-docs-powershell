---
title: "Add-SPServiceApplicationProxyGroupMember"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 25ccffa1-84ae-4927-a1e5-4b2d55f6065f

description: "Adds a member to the service application proxy group."
---

# Add-SPServiceApplicationProxyGroupMember

Adds a member to the service application proxy group.
  
```
Add-SPServiceApplicationProxyGroupMember [-Identity] <SPServiceApplicationProxyGroupPipeBind> [-Member] <SPServiceApplicationProxyPipeBind[]> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Add-SPServiceApplicationProxyGroupMember** cmdlet adds a member to the service application proxy group. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |SPServiceApplicationProxyGroupPipeBind.  <br/> |Specifies the service application proxy group to which to add the member.  <br/> |
|**Member** <br/> |Required  <br/> |SPServiceApplicationProxyPipeBind[]  <br/> |Specifies an array of members to add to the service application proxy group.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> ||
|**Member** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind[]  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Add-SPServiceApplicationProxyGroupMember RemoteProxyGroup -Member babab30e-8e3a-428b-8ff4-4d5c8f455e6d
```

This example adds a select service application proxy to the service application proxy group named  `RemoteProxyGroup`.
  
The service application proxy group GUID is unique to every farm. You can run Get-SPServiceApplicationProxyGroup | Select Name,Id to see the GUID of the serviceapplication proxy groups. Use this result for any other **SPServiceApplicationProxyGroup** cmdlets. 
  
## See also

#### 

[Remove-SPServiceApplicationProxyGroupMember](remove-spserviceapplicationproxygroupmember.md)

