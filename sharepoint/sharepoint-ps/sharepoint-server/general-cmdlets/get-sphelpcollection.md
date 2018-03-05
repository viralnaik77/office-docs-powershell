---
title: "Get-SPHelpCollection"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 91d0ffff-0a0c-45eb-aba1-280891387fff

description: "Returns Help collection files."
---

# Get-SPHelpCollection

Returns Help collection files.
  
```
Get-SPHelpCollection [-AssignmentCollection <SPAssignmentCollection>] [-Name <String>]
```

## Detailed Description

The **Get-SPHelpCollection** cmdlet reads the specified Help collection files. If the **Name** parameter is not specified, this cmdlet returns all installed Help collection files. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the Help collection files to get.  <br/> The type must be a valid name of a Help collection folder; for example, HelpDocs1.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
Get-SPHelpCollection
```

This example gets all installed Help collection files.
  
## See also

#### 

[Install-SPHelpCollection](install-sphelpcollection.md)
  
[Uninstall-SPHelpCollection](uninstall-sphelpcollection.md)

