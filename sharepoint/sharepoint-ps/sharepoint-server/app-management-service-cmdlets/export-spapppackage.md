---
title: "Export-SPAppPackage"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5862a43e-d0e3-4b4c-9ca6-3581c38dc821

description: "Exports an app package."
---

# Export-SPAppPackage

Exports an app package.
  
```
Export-SPAppPackage -App <SPApp> -Path <String> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Export-SPAppPackage** cmdlet to export an app package from the content database. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**App** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPApp  <br/> |Specifies the App for which to export the package.  <br/> |
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the path of the exported file.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**App** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPApp  <br/> ||
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE-----------
  
```
$instance = Get-SPAppInstance -AppInstanceId 5b14e3d9-aaa6-4c12-a762-601c9864552c
Export-SPAppPackage -App $instance.App -Path .\exported.spapp

```

This example exports an app package with the ID "5b14e3d9-aaa6-4c12-a762-601c9864552c" to the **exported.spapp** file in the current directory. 
  
## See also

#### 

[Import-SPAppPackage](import-spapppackage.md)

