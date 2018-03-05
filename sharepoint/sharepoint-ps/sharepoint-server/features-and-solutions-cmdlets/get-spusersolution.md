---
title: "Get-SPUserSolution"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/8/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d1850213-8dc8-483f-befc-7d8f7ac349ab

description: "Returns a specified sandboxed solution."
---

# Get-SPUserSolution

Returns a specified sandboxed solution.
  
```
Get-SPUserSolution [[-Identity] <SPUserSolutionPipeBind>] -Site <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPUserSolution** cmdlet returns a specified sandboxed solution. If the **Identity** parameter is not specified, this cmdlet returns the collection of sandboxed solutions in the site collection. A user solution is a sandboxed solution. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserSolutionPipeBind  <br/> |Specifies the sandboxed solution to get.  <br/> The type must be a valid name of a user solution (for example, UserSolution1); or an instance of a valid **SPUserSolution** object.  <br/> |
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the site collection that contains the sandboxed solution.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form http://server_name; or an instance of a valid **SPSite** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserSolutionPipeBind  <br/> ||
|**Site** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-----------------EXAMPLE---------------------
  
```
Get-SPUserSolution -Site http://sitename
```

This example displays information about sandboxed solutions in the site  `http://sitename`.
  
## See also

#### 

[Update-SPUserSolution](update-spusersolution.md)
  
[Install-SPUserSolution](install-spusersolution.md)
  
[Uninstall-SPUserSolution](uninstall-spusersolution.md)
  
[Remove-SPUserSolution](remove-spusersolution.md)
  
[Add-SPUserSolution](add-spusersolution.md)

