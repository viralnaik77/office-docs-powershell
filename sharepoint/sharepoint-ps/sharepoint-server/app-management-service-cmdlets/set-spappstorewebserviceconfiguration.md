---
title: "Set-SPAppStoreWebServiceConfiguration"
ms.author: kirks
author: Techwriter40
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84351a4c-fe0f-4c0d-89e0-af50f793efce

description: "Sets properties of a SharePoint Store app."
---

# Set-SPAppStoreWebServiceConfiguration

Sets properties of a SharePoint Store app.
  
```
Set-SPAppStoreWebServiceConfiguration -Client <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ProxyVersion <Version>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------EXAMPLE-------
  
```
Set-SPAppStoreWebServiceConfiguration -Client=SP -ProxyVersion=16.1
```

This example set the product type and version for a SharePoint Store app.
  
## Detailed Description

Use the **Set-SPAppStoreWebServiceConfiguration** cmdlet to set the product type (On-Premises or Online) and the version used to access the SharePoint Store when SharePoint is configured to access the . 
  
> [!NOTE]
> This cmdlet is not intended for the ITPro audience. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Client_ <br/> |Required  <br/> |System.String  <br/> |Specifies the client value of the SharePoint Store app.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ProxyVersion_ <br/> |Optional  <br/> |System.Version  <br/> |Specifies the proxy version value of the SharePoint Store app.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPAppStoreWebServiceConfiguration](get-spappstorewebserviceconfiguration.md)

