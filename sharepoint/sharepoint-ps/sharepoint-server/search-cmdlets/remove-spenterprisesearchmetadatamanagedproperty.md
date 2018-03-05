---
title: "Remove-SPEnterpriseSearchMetadataManagedProperty"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0d1e9ea8-2e36-4e9a-9fa8-1ab6dc4c29b1

description: "Deletes a metadata managed property."
---

# Remove-SPEnterpriseSearchMetadataManagedProperty

Deletes a metadata managed property.
  
```
Remove-SPEnterpriseSearchMetadataManagedProperty -Identity <ManagedPropertyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SearchApplication <SearchServiceApplicationPipeBind>] [-SiteCollection <Guid>] [-Tenant <Guid>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication
```

```
$mp = Get-SPEnterpriseSearchMetadataManagedProperty -SearchApplication $searchapp -Identity AboutMeUpdate

```

```
Remove-SPEnterpriseSearchMetadataManagedProperty -Identity $mp
```

This example removes the managed property  `AboutMeUpdate` from the default search service application. 
  
## Detailed Description

This cmdlet deletes a specified managed property from the managed property collection.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> |Specifies the managed property to delete.  <br/> The type must be a valid name of a managed property, for example ManagedProperty1, or an instance of a valid **ManagedProperty** object.  <br/> Note that if only a name of a managed property is specified, a **SearchApplication** must also be specified.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the managed property collection.  <br/> The type must be a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _SiteCollection_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the managed properties returned are to be within the scope of a site collection (SPSite).  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _Tenant_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies that the managed properties returned are to be within the scope of a tenant.  <br/> The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ManagedPropertyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**SiteCollection** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**Tenant** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchMetadataManagedProperty](get-spenterprisesearchmetadatamanagedproperty.md)
  
[New-SPEnterpriseSearchMetadataManagedProperty](new-spenterprisesearchmetadatamanagedproperty.md)
  
[Set-SPEnterpriseSearchMetadataManagedProperty](set-spenterprisesearchmetadatamanagedproperty.md)

