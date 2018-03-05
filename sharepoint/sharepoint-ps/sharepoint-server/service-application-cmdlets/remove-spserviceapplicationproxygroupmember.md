---
title: "Remove-SPServiceApplicationProxyGroupMember"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12545ac4-2bed-433e-aed5-b56bfb95c631

description: "Removes one or more proxies from the specified service application proxy group."
---

# Remove-SPServiceApplicationProxyGroupMember

Removes one or more proxies from the specified service application proxy group.
  
```
Remove-SPServiceApplicationProxyGroupMember [-Identity] <SPServiceApplicationProxyGroupPipeBind> [-Member] <SPServiceApplicationProxyPipeBind[]> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Remove-SPServiceApplicationProxyGroupMember** cmdlet removes one or more proxies from the specified service application proxy group. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> |Specifies the identity of the service application proxy group from which to remove the member or members.  <br/> |
|**Member** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind[]  <br/> |Specifies the member or members to remove from the service application proxy group.  <br/> |
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
Remove-SPServiceApplicationProxyGroupMember RemoteProxyGroup -Member babab30e-8e3a-428b-8ff4-4d5c8f455e6d
```

This example removes a service application proxy from the selected service application proxy group named  `RemoteProxyGroup`.
  
The service application proxy group GUID is unique to every farm. You can run Get-SPServiceApplicationProxyGroup | Select Name,Id to see the GUID of the service application proxy groups. Use this result for any other **SPServiceApplicationProxyGroup** cmdlets. 
  
## See also

#### 

[Add-SPServiceApplicationProxyGroupMember](add-spserviceapplicationproxygroupmember.md)

