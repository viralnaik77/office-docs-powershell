---
title: "Remove-SPSiteMaster"
ms.author: kirks
author: Techwriter40
ms.date: 10/23/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d722f73a-448c-47c1-913c-b0bb0dd5aa36

description: "Removes a site master."
---

# Remove-SPSiteMaster

Removes a site master.
  
```
Remove-SPSiteMaster -ContentDatabase <SPContentDatabasePipeBind> -SiteId <Guid> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE-----------------------
  
```
Remove-SPSiteMaster -ContentDatabase "WSS_Content" -SiteId 
```

This example removes a site master from the database.
  
## Detailed Description

Use the **Remove-SPSiteMaster** cmdlet to remove a site master from the database. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ContentDatabase_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the name of the database to remove the site master. For example, WSS_Content.  <br/> |
| _SiteId_ <br/> |Required  <br/> |System.Guid  <br/> |Specifies the ID of the Site Master to remove. For example, ff480534-7e64-44a5-b7e3-7c418624cdf6.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPSiteMaster](get-spsitemaster.md)
  
[New-SPSiteMaster](new-spsitemaster.md)

