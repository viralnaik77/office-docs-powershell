---
title: "Remove-SPAppDeniedEndpoint"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 647663f9-1376-4365-bb93-5215a2702ba2

description: "Removes a relative URL endpoint of a server from the list of app-denied endpoints."
---

# Remove-SPAppDeniedEndpoint

Removes a relative URL endpoint of a server from the list of app-denied endpoints.
  
```
Remove-SPAppDeniedEndpoint [-Endpoint] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Remove-SPAppDeniedEndpoint** cmdlet to remove a relative URL endpoint of a server from the list of app-denied endpoints. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Endpoint** <br/> |Required  <br/> |System.String  <br/> |Specifies a relative URL endpoint of a server that will be removed from the list of app-denied endpoints. Apps will not be able to access relative URL endpoints of a server that exist in the app-denied endpoint list.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Endpoint** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------EXAMPLE----------
  
```
Remove-SPAppDeniedEndpoint -Endpoint "/_vti_bin/contoso/service.asmx"
```

This example removes the **"/_vti_bin/contoso/service.asmx"** endpoint from the list of denied endpoints for apps. Apps will be able to access this endpoint because it is being removed from the app-denied endpoint list. 
  
## See also

#### 

[Get-SPServiceApplicationEndpoint](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/service-application-cmdlets/get-spserviceapplicationendpoint.md)
  
[Remove-SPAppDeniedEndpoint](remove-spappdeniedendpoint.md)
  
[Set-SPServiceApplicationEndpoint](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/service-application-cmdlets/set-spserviceapplicationendpoint.md)

