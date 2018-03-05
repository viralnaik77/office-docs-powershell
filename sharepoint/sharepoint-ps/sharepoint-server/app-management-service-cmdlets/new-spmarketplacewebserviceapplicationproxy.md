---
title: "New-SPMarketplaceWebServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 99ea6e90-9257-43c1-b16a-59693cd3c99c

description: "Creates a service application proxy for the app identity data web service."
---

# New-SPMarketplaceWebServiceApplicationProxy

Creates a service application proxy for the app identity data web service.
  
```
New-SPMarketplaceWebServiceApplicationProxy -Name <String> -ServiceEndpointUri <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DefaultProxyGroup <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **New-SPMarketplaceWebServiceApplicationProxy** cmdlet to create a service application proxy for the app identity data web service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the service application proxy.  <br/> |
|**ServiceEndpointUri** <br/> |Required  <br/> |System.String  <br/> |Specifies the URI of the app identity data web service.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to add the service application proxy to the default proxy group.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**ServiceEndpointUri** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------EXAMPLE--------
  
```
New-SPMarketplaceWebServiceApplicationProxy -Name ApplicationIdentityData -ServiceEndpointUri http://server:7800/ApplicationIdentityData.svc -DefaultProxyGroup
```

This example adds a proxy named ApplicationIdentityData to the app identity web service.
  

