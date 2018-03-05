---
title: "Get-SPUserLicenseMapping"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89c0fc67-9a64-4360-88cc-af83c07ce347

description: "Returns the claim-to-user license mappings."
---

# Get-SPUserLicenseMapping

Returns the claim-to-user license mappings.
  
```
Get-SPUserLicenseMapping [-AssignmentCollection <SPAssignmentCollection>] [-WebApplication <SPWebApplicationPipeBind>]
```

## Detailed Description

The **Get-SPUserLicenseMapping** cmdlet returns the claim-to-user license mappings for the entire SharePoint farm or a specific web application. 
  
> [!NOTE]
> Getting the mappings for the entire farm does not retrieve any specific mappings on a web application. 
  
If you specify no parameters, the license mappings for the entire farm are returned. To display the license mappings for a specific web application, use the **WebApplication** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the URL, GUID, web application name, or instance of a web application object from which to get the user license mappings. The type must be an URL in the form http://server_name or http://server_name/sites/sitename, a valid GUID (for example, 12345678-90ab-cdef-1234-567890bcdefgh), a web application name (that is, SharePoint - 80), or an instance of a web application object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
   
## Example

---------------EXAMPLE 1-----------------
  
```
Get-SPUserLicenseMapping
```

This example returns all claim-to-user license mappings for the entire SharePoint farm.
  
---------------EXAMPLE 2 -----------------
  
```
Get-SPUserLicenseMapping -WebApplication "SharePoint - 80"
```

This example returns all claim-to-user license mappings for the web application with the name "SharePoint - 80".
  
---------------EXAMPLE 3 -----------------
  
```
Get-SPUserLicenseMapping -WebApplication http://<server_name>/sitename
```

This example returns all claim-to-user license mappings for the Web application with the URL http://\<server_name\>/sites/sitename.
  
## See also

#### 

[Add-SPUserLicenseMapping](add-spuserlicensemapping.md)
  
[Remove-SPUserLicenseMapping](remove-spuserlicensemapping.md)

