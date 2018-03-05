---
title: "Get-SPWebPartPack"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a002b0f1-0c9c-4be6-b8ff-cb42b7b1dc29

description: "Returns the Web Part packages that were installed for the specified scope."
---

# Get-SPWebPartPack

Returns the Web Part packages that were installed for the specified scope.
  
```
Get-SPWebPartPack [[-Identity] <String>] [-AssignmentCollection <SPAssignmentCollection>] [-GlobalOnly <SwitchParameter>] [-WebApplication <SPWebApplicationPipeBind>]
```

## Detailed Description

The **Get-SPWebPartPack** cmdlet returns the installed Web Part packages that match the **Identity** parameter. The scope of results can be narrowed by using the optional **WebApplication** parameter. The scope does not include any Web Part packages installed in the global assembly cache (GAC) unless the **GlobalOnly** parameter is used. If this parameter is used, only Web Part packages that have been installed in the GAC are returned. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |System.String  <br/> |Specifies the full or partial name of the Web Part package from the configuration database.  <br/> The type must be a valid name of a Web Part package; for example, MyWebPartPackage.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**GlobalOnly** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Returns only Web Part packages that are installed in the global assembly cache (GAC).  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the Web application from which to list Web Part packages. If no Web application is specified, the specified Web Part packages will be returned from all Web applications.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**GlobalOnly** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Get-SPWebPartPack -WebApplication http://zsharepoint2:80
```

This example returns all Web Part packages that have been installed on the Web application on port  `80` in local farm. 
  
## See also

#### 

[Install-SPWebPartPack](install-spwebpartpack.md)
  
[Uninstall-SPWebPartPack](uninstall-spwebpartpack.md)

