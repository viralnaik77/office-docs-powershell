---
title: "Get-SPAuthenticationRealm"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7ec6c10c-283e-4533-addf-6bdd2d804c28

description: "Returns the authentication realm ID for the entire farm or for a specific site in a site subscription."
---

# Get-SPAuthenticationRealm

Returns the authentication realm ID for the entire farm or for a specific site in a site subscription.
  
```
Get-SPAuthenticationRealm [[-ServiceContext] <SPServiceContextPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPAuthenticationRealm** cmdlet to display the authentication realm ID of the farm or for a specific site in a site subscription. In environments where site subscriptions have been set up, you can use the **-ServiceContext** parameter and the full URL for a site in the site subscription to get the authentication realm ID for that site subscription. If you have not set up site subscriptions, the **-ServiceContext** parameter will have no effect and will return the farm authentication realm ID. By default, the farm authentication realm ID is the same as the farm ID. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the full URL of a site in a site subscription for which the realm ID needs to be displayed.  <br/> > [!NOTE]> If the site specified in with the parameter is a part of a site subscription, then the cmdlet will return the authentication realm ID for the site subscription. Otherwise, the cmdlet will return the authentication realm ID for the farm.           |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

----------------EXAMPLE-------------
  
```
Get-SPAuthenticationRealm
```

This example displays the authentication realm ID for the entire farm.
  
## See also

#### 

[Set-SPAuthenticationRealm](set-spauthenticationrealm.md)

