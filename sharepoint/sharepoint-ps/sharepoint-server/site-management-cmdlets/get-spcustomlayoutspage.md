---
title: "Get-SPCustomLayoutsPage"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9fb76a22-15d3-4d2e-bf78-9bec4ca45bb4

description: "Returns a mapping to a custom layout page."
---

# Get-SPCustomLayoutsPage

Returns a mapping to a custom layout page.
  
```
Get-SPCustomLayoutsPage -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <Int32>] [-Identity <None | AccessDenied | Confirmation | Error | Login | RequestAccess | Signout | WebDeleted>]

```

## Example

------------------EXAMPLE-----------------------
  
```
Get-SPCustomLayoutsPage -Identity "_layouts/accessdenied.aspx" -WebApplication "http://server_name/mywebapp"
```

This example returns the mapping of the  `AccessDenied` layout page in the Web application. 
  
## Detailed Description

The **Get-SPCustomLayoutsPage** cmdlet returns a mapping to a custom layout page in a Web application. If the **Identity** parameter is not specified, this cmdlet returns the collection of mappings for all custom layout pages. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _WebApplication_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the SharePoint Web application that contains the custom layout page.  <br/> The type must be a valid URL, in the form http://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CompatibilityLevel_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the version of templates to use when creating a new **SPSite** object. This value sets the initial CompatibilityLevel value for the site collection. When this parameter is not specified, the CompatibilityLevel will default to the highest possible version for the web application depending on the CompatibilityRange setting.  <br/> |
| _Identity_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPWebApplication+SPCustomPage  <br/> |Specifies the custom layout page to get.  <br/> The type must be one of the following: **None**, **AccessDenied**, **Confirmation**, **Error**, **Login**, **RequestAccess**, **Signout**, or **WebDeleted**.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPWebApplication+SPCustomPage  <br/> ||
   
## See also

#### 

[Set-SPCustomLayoutsPage](set-spcustomlayoutspage.md)

