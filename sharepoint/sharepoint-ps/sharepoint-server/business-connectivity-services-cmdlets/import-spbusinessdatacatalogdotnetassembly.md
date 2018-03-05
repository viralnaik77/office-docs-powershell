---
title: "Import-SPBusinessDataCatalogDotNetAssembly"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 05615c01-f5b1-407f-9e9a-43e44c85ff90

description: "Imports a .NET Connectivity assembly."
---

# Import-SPBusinessDataCatalogDotNetAssembly

Imports a .NET Connectivity assembly.
  
```
Import-SPBusinessDataCatalogDotNetAssembly -LobSystem <LobSystem> -Path <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DependentAssemblyPaths <String[]>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Import-SPBusinessDataCatalogDotNetAssembly** cmdlet imports a .NET Connectivity Assembly that corresponds to a .NET Assembly Connector and LobSystem in the metadata store. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**LobSystem** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.LobSystem  <br/> |Specifies the LobSystem that the assembly corresponds to.  <br/> |
|**Path** <br/> |Required  <br/> |System.String  <br/> |Specifies the path to the primary assembly.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DependentAssemblyPaths** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies a list of paths to dependent assemblies.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**LobSystem** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.Administration.LobSystem  <br/> ||
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DependentAssemblyPaths** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------------EXAMPLE 1----------------
  
```
Import-SPBusinessDataCatalogDotNetAssembly -LobSystem $ContosoDB -Path "c:\Folder\Assembly.dll"
```

This example imports the assembly  `Assembly`.
  
-----------------EXAMPLE 2----------------
  
```
Import-SPBusinessDataCatalogDotNetAssembly -LobSystem $ContosoDB -Path "c:\Folder\Assembly.dll" -DependentAssemblyPaths "c:\Folder\Assembly2.dll","c:\Folder\Assembly3.dll"
```

This example imports the assembly  `Assembly`, and also imports the dependent assemblies  `Assembly2` and  `Assembly3`.
  

