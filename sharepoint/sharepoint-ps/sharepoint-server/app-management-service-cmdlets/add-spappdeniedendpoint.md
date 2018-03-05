---
title: "Add-SPAppDeniedEndpoint"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7d5d96c3-be7f-47e0-a4f7-8610f29adfa4

description: "Adds a relative URL endpoint of a server to the list of app-denied endpoints."
---

# Add-SPAppDeniedEndpoint

Adds a relative URL endpoint of a server to the list of app-denied endpoints.
  
```
Add-SPAppDeniedEndpoint [-Endpoint] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Add-SPAppDeniedEndpoint** cmdlet to add a relative URL endpoint of a server to the list of app-denied endpoints in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Endpoint** <br/> |Required  <br/> |System.String  <br/> |Specifies a relative URL endpoint of a server that is added to the list of app-denied endpoints. Apps will not be able to access relative URL endpoints of a server that exist in the app-denied endpoint list.  <br/> |
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

-------------EXAMPLE-------------
  
```
Add-SPAppDeniedEndpoint -Endpoint "/_vti_bin/contoso/service.asmx"
```

This example adds the **"/_vti_bin/contoso/service.asmx"** endpoint to the list of denied endpoints for apps. Apps will not be able to access this endpoint. 
  
## See also

#### 

[Remove-SPAppDeniedEndpoint](remove-spappdeniedendpoint.md)
  
[Set-SPServiceApplicationEndpoint](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/service-application-cmdlets/set-spserviceapplicationendpoint.md)
#### 

[Clear-SPAppDeniedEndpoints](http://technet.microsoft.com/library/0ed45c68-dc70-4d6e-b13a-dee87620ff99.aspx)
  
[Get-SPAppDeniedEndpoints](http://technet.microsoft.com/library/fad7a182-1abc-4238-898d-ab56afb75c88.aspx)

