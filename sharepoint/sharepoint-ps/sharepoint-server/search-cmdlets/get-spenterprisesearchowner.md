---
title: "Get-SPEnterpriseSearchOwner"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45f4323d-6bc8-4be9-a8da-584f8d1b9f7b

description: "Retrieves the search object owner."
---

# Get-SPEnterpriseSearchOwner

Retrieves the search object owner.
  
```
Get-SPEnterpriseSearchOwner -Level <SPWeb | SPSite | SPSiteSubscription | Ssa> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <SearchObjectOwner>] [-SPWeb <SPWebPipeBind>]

```

## Example

--------EXAMPLE--------
  
```
$tenantOwner = Get-SPEnterpriseSearchOwner -Level SPSite
```

This example shows how to retrieve the tenant owner of a search object at the SPSite level.
  
## Detailed Description

The **Get-SPEnterpriseSearchOwner** cmdlet retrieves the search object owner. **Get-SPEnterpriseSearchOwner** provides scoping context to other cmdlets such as SPEnterpriseSearchResultItemType. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Level_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectLevel  <br/> |Specifies whether the owner object resides at the SPWeb, SPSite, SPSite Subscription, or SSA level.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> |Specifies the search object owner to retrieve.  <br/> |
| _SPWeb_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the SPWeb or SPSite in which this object resides. It is only needed if **Level** is equal to SPWeb or SPSite.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectOwner  <br/> ||
|**Level** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.SearchObjectLevel  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SPWeb** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
   

