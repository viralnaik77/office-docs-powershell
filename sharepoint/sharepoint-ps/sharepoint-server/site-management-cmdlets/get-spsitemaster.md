---
title: "Get-SPSiteMaster"
ms.author: kirks
author: Techwriter40
ms.date: 6/8/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc2948dc-fd0b-4d1f-b191-55ee0e90d08a

description: "Returns site master information."
---

# Get-SPSiteMaster

Returns site master information.
  
```
Get-SPSiteMaster -ContentDatabase <SPContentDatabasePipeBind> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------------EXAMPLE-----------------------
  
```
Get-SPSiteMaster -ContentDatabase WSS_Content
```

This example returns the site master in the database WSS_Content.
  
## Detailed Description

Use the **Get-SPSiteMaster** cmdlet to display site master information in the farm. 
  
Typically the following information is displayed:
  
- ContentDatabase
    
- SiteId
    
- TemplateName
    
- Language
    
- CompatibilityLevel
    
- FeaturesToActivateOnCopy
    
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ContentDatabase_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the name of the database to get the list of Site Masters. For example, WSS_Content.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## See also

#### 

[New-SPSiteMaster](new-spsitemaster.md)
  
[Remove-SPSiteMaster](remove-spsitemaster.md)

