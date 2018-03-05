---
title: "Export-SPMetadataWebServicePartitionData"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5024af80-0333-4d64-90d0-f60423c7799d

description: "Exports the data from a metadata Web service for a site subscription."
---

# Export-SPMetadataWebServicePartitionData

Exports the data from a metadata Web service for a site subscription.
  
```
Export-SPMetadataWebServicePartitionData -Identity <SPSiteSubscriptionPipeBind> -Path <String> -ServiceProxy <SPMetadataServiceProxyCmdletPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-NoCompression <SwitchParameter>]

```

## Example

-----------------EXAMPLE--------------
  
```
Export-SPMetadataWebServicePartitionData -Identity $siteSubscriptionPipeBind1 -ServiceProxy "MetadataServiceProxy2" -Path "\\server_name\folder_name\file_name.cab"
```

This example creates a backup of data for a specific site subscription on a Metadata Service application.
  
## Detailed Description

Use the **Export-SPMetadataWebServicePartitionData** cmdlet to export the data from a metadata Web service that is associated with the specified site subscription. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
> [!TIP]
> To find the GUID of an object look use the GET command. For more information on the GET command look here: [Get-SPFeature](https://technet.microsoft.com/en-us/library/ff607945)
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site subscription to export.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a site subscription (for example, SiteSubscriptionConfig1); or an instance of a valid **SiteSubscription** object.  <br/> |
| _Path_ <br/> |Required  <br/> |System.String  <br/> |Specifies the path and file name for the file to create from the exported data.  <br/> The type must be a valid path in either of the following forms:  <br/> - C:\folder_name\subscription_export  <br/> - \\server_name\folder_name\file_name.cab  <br/> |
| _ServiceProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> |Specifies the service proxy for the service application that contains the site subscription.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of the service application proxy (for example, ServiceAppProxy1); or an instance of a valid **SPMetadataServiceProxy** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _NoCompression_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |PARAMVALUE: SwitchParameter  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**ServiceProxy** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> ||
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Clear-SPMetadataWebServicePartitionData](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/clear-spmetadatawebservicepartitiondata.md)
  
[Import-SPMetadataWebServicePartitionData](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/import-spmetadatawebservicepartitiondata.md)

