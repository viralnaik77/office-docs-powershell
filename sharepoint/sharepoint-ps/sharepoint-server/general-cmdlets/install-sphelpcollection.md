---
title: "Install-SPHelpCollection"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 489c518b-9d3b-4016-b2a7-5dd4c8ed041a

description: "Installs the provided Help site collection files in the current farm."
---

# Install-SPHelpCollection

Installs the provided Help site collection files in the current farm.
  
```
Install-SPHelpCollection -LiteralPath <String> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Install-SPHelpCollection** cmdlet installs the Help site collection files for SharePoint 2013 in the current farm. Use the **LiteralPath** parameter to install specific custom Help collection files. If the **LiteralPath** parameter is not specified, all available Help in the Help site collection is installed and existing Help collection files are overwritten. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**All** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |If the **LiteralPath** parameter is not specified, specifies that all Help Collection CABs under **%Program Files%\Common Files\Microsoft Shared\Web Server Extensions\15\HCCab\\<LCID\>** in the Help site collection are installed, and existing Help collections are overwritten.  <br/> |
|**LiteralPath** <br/> |Required  <br/> |System.String  <br/> |Specifies the exact path to a specific custom Help file in the Help site collection cab file.  <br/> The type must be a valid path in either of the following forms:  <br/> - C:\folder_name  <br/> - \\server_name\folder_name  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## Example

------------------EXAMPLE------------------
  
```
Install-SPHelpCollection -LiteralPath 'C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\HCCab\1033\OSSAdmin.cab' 
```

This example installs the specified help collection in the current farm.
  
## See also

#### 

[Get-SPHelpCollection](get-sphelpcollection.md)
  
[Uninstall-SPHelpCollection](uninstall-sphelpcollection.md)

