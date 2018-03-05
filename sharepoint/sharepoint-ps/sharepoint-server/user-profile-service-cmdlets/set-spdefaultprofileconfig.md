---
title: "Set-SPDefaultProfileConfig"
ms.author: kirks
author: Techwriter40
ms.date: 12/8/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86c28cce-ea47-4c3e-8880-065f10ad1f4e

description: "Changes the MySitesPublicEnabled property of the User Profile Application Proxy ."
---

# Set-SPDefaultProfileConfig

Changes the MySitesPublicEnabled property of the User Profile Application Proxy .
  
```
Set-SPDefaultProfileConfig -MySitesPublicEnabled <$true | $false> -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

---------------EXAMPLE------------ 
  
```
$upaProxy = Get-SPServiceApplicationProxy 1232b6f7-b9ff-99ad-0cd0-fg1g67h981aq
```

```
Set-SPDefaultProfileConfig $upa -MySitesPublicEnabled $true
```

This example changes the MySitesPublicEnabled property of the specified user profile service application. 
  
## Detailed Description

Use the **Set-SPDefaultProfileConfig** cmdlet to change the MySitesPublicEnabled property of a User Profile Application Proxy from whatever was set at the time of Proxy creation to whatever is defined by using this cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _MySitesPublicEnabled_ <br/> |Required  <br/> |System.Boolean  <br/> |Enables or disables public MySites.  <br/> The valid values are **$True** or **$False**.  <br/> |
| _ProfileServiceApplicationProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the proxy of the User Profile Service application that contains the site subscription to delete.The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a service application proxy (for example, UserProfileSvcProxy1); or an instance of a valid SPServiceApplicationProxy object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   

