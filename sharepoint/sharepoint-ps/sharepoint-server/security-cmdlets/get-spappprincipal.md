---
title: "Get-SPAppPrincipal"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/20/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7fda9d75-b44b-46e4-b471-69a8ae8df27e

description: "Displays a specific app principal object."
---

# Get-SPAppPrincipal

Displays a specific app principal object.
  
```
Get-SPAppPrincipal -NameIdentifier <String> -Site <SPWebPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPAppPrincipal** cmdlet to display a specific app principal object from the SharePoint app registry. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**NameIdentifier** <br/> |Required  <br/> |System.String  <br/> |Specifies the app principal's name identifier to search for.  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the name of the site for the app principal object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**NameIdentifier** <br/> |Required  <br/> |System.String  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-----------EXAMPLE--------
  
```
Get-SPAppPrincipal -NameIdentifier "00000003-0000-0ff1-ce00-000000000000@f686d426-8d16-42db-81b7-cb578e110ccd"
```

This example returns the app principal for a specified ID.
  
## See also

#### 

[Register-SPAppPrincipal](register-spappprincipal.md)

