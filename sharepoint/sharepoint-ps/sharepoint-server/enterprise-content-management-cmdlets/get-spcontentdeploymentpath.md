---
title: "Get-SPContentDeploymentPath"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3cc27778-5902-486a-8bc4-1cba5424ca86

description: "Returns a content deployment path or a collection of content deployment paths."
---

# Get-SPContentDeploymentPath

Returns a content deployment path or a collection of content deployment paths.
  
```
Get-SPContentDeploymentPath [-AssignmentCollection <SPAssignmentCollection>] [-Identity <SPContentDeploymentPathPipeBind>]

```

## Example

--------------EXAMPLE--------------
  
```
Get-SPContentDeploymentPath "Path 1"
```

This example returns the content deployment path named  `Path1`. 
  
## Detailed Description

The **Get-SPContentDeploymentPath** cmdlet reads the specified content deployment path. If the **Identity** parameter is not specified, this cmdlet returns the collection of content deployment paths on the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Cmdlet.SPContentDeploymentPathPipeBind  <br/> |Specifies the content deployment path to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a content deployment path (for example, DeployPath1); or an instance of a valid **SPContentDeploymentJob** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Cmdlet.SPContentDeploymentPathPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPContentDeploymentPath](new-spcontentdeploymentpath.md)
  
[Remove-SPContentDeploymentPath](remove-spcontentdeploymentpath.md)
  
[Set-SPContentDeploymentPath](set-spcontentdeploymentpath.md)

