---
title: "Get-SPUserSettingsProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a8d0c58a-afaf-4b24-a8f8-baacf1f37816

description: "Returns a list of User Settings Providers installed on the farm."
---

# Get-SPUserSettingsProvider

Returns a list of User Settings Providers installed on the farm.
  
```
Get-SPUserSettingsProvider [[-Identity] <SPUserSettingsProviderPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPUserSettingsProvider** cmdlet to return a list of User Settings Providers. To return a list of a specific user setting provider, use the **Identity** parameter. Otherwise, the list for the entire farm is returned. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserSettingsProviderPipeBind  <br/> |Specifies the GUID ID for a User Settings Provider.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserSettingsProviderPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-----------EXAMPLE--------
  
```
$provider = Get-SPUserSettingsProvider
```

```
$site = Get-SPSite -Identity http://someserver
```

```
$user = $site.RootWeb.CurrentUser
```

```
ctx = $provider.GetProviderContext($user)
```

```
$provider.GetUserRegionalSettings($ctx,$user)
```

This example returns the regional settings for a specified user.
  
## See also

#### 

[New-SPUserSettingsProvider](new-spusersettingsprovider.md)
  
[Remove-SPUserSettingsProvider](remove-spusersettingsprovider.md)
  
[Get-SPUserSettingsProviderManager](get-spusersettingsprovidermanager.md)

