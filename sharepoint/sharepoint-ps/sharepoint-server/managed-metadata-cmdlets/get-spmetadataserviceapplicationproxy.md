---
title: "Get-SPMetadataServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45766f63-629f-4f82-982e-0614280a4948

description: "Returns an existing connection to a managed metadata service application, which is also known as a proxy, to the managed metadata service application."
---

# Get-SPMetadataServiceApplicationProxy

Returns an existing connection to a managed metadata service application, which is also known as a proxy, to the managed metadata service application.
  
```
Get-SPMetadataServiceApplicationProxy [-Identity] <SPMetadataServiceProxyCmdletPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

Use the **Get-SPMetadataServiceApplicationProxy** cmdlet to get a specified connection to a managed metadata service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> |Specifies the service application proxy to read.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of the service application proxy (for example, ServiceAppProxy1); or an instance of a valid **SPMetadataServiceProxy** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

----------------EXAMPLE-------------
  
```
Get-SPMetadataServiceApplicationProxy -Identity "MetadataServiceProxy1"
```

This example retrieves an existing connection to a managed metadata service application.
  
## See also

#### 

[New-SPMetadataServiceApplicationProxy](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/enterprise-content-management-cmdlets/new-spmetadataserviceapplicationproxy.md)
  
[Set-SPMetadataServiceApplicationProxy](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/enterprise-content-management-cmdlets/set-spmetadataserviceapplicationproxy.md)

