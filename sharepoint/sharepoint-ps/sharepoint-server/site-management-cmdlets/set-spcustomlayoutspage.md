---
title: "Set-SPCustomLayoutsPage"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8d0b221d-7249-4c7c-a13c-74a0994c3d54

description: "Maps a new path for a custom layout page."
---

# Set-SPCustomLayoutsPage

Maps a new path for a custom layout page.
  
```
Set-SPCustomLayoutsPage -RelativePath <String> [-CompatibilityLevel <Int32>] <COMMON PARAMETERS>

```

## Example

------------------EXAMPLE-----------------------
  
```
Set-SPCustomLayoutsPage -Identity AccessDenied -RelativePath "/_layouts/custompages/myaccessdenied.aspx" -WebApplication "http://server_name/mywebapp"
```

This example maps the specified path for the AccessDenied layout page in the Web application  `"http://server_name/mywebapp"`.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **Set-SPCustomLayoutsPage** cmdlet maps a new path for a custom layouts page in a Web application. To remove the mapping for a custom layouts page, use the ** Reset ** parameter instead of the **RelativePath** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPWebApplication+SPCustomPage  <br/> |Specifies the custom layout page to set.  <br/> The type must be one of the following: **None**, **AccessDenied**, **Confirmation**, **Error**, **Login**, **RequestAccess**, **Signout**, or **WebDeleted**.  <br/> |
| _RelativePath_ <br/> |Required  <br/> |System.String  <br/> |Specifies the path of the custom layout page.  <br/> The type must be a valid path of a layout page, in the form _layouts/custompages/myaccessdenied.aspx.  <br/> |
| _Reset_ <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Sets the mapping of a custom layouts page to NULL.  <br/> |
| _WebApplication_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the SharePoint Web application that contains the custom layout page.  <br/> The type must be a valid URL, in the form http://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid **SPWebApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CompatibilityLevel_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the version of templates to use when creating a new **SPSite** object. This value sets the initial CompatibilityLevel value for the site collection. When this parameter is not specified, the CompatibilityLevel will default to the highest possible version for the web application depending on the CompatibilityRange setting.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPWebApplication+SPCustomPage  <br/> ||
|**RelativePath** <br/> |Required  <br/> |System.String  <br/> ||
|**Reset** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPCustomLayoutsPage](get-spcustomlayoutspage.md)

