---
title: "Clear-SPMetadataWebServicePartitionData"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4b175caf-ca3c-4f4c-b6cb-b92acc367d95

description: "Removes all data for a site subscription on a metadata Web service application."
---

# Clear-SPMetadataWebServicePartitionData

Removes all data for a site subscription on a metadata Web service application.
  
```
Clear-SPMetadataWebServicePartitionData -Identity <SPSiteSubscriptionPipeBind> <COMMON PARAMETERS>

```

## Example

----------------EXAMPLE---------------
  
```
Clear-SPMetadataWebServicePartitionData -Identity $siteSubscriptionPipeBind1 -ServiceProxy "MetadataServiceProxy2"
```

This example removes data for a site subscription on a Metadata Service application.
  
## Detailed Description

Use the **Clear-SPMetadataWebServicePartitionData** cmdlet to clear all data for a site subscription on a metadata Web service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site subscription configuration to remove.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a site subscription (for example, SiteSubscriptionConfig1); or an instance of a valid **SiteSubscription** object.  <br/> |
| _ServiceContext_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |PARAMVALUE: SPServiceContextPipeBind  <br/> |
| _ServiceProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> |Specifies the service proxy for the service application that contains the site subscription.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of the service application proxy (for example, ServiceAppProxy1); or an instance of a valid **SPMetadataServiceProxy** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _FromContentDatabase_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |PARAMVALUE: SPContentDatabasePipeBind  <br/> |
| _FromServiceDatabase_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |PARAMVALUE: SwitchParameter  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**ServiceProxy** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[Export-SPMetadataWebServicePartitionData](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/enterprise-content-management-cmdlets/export-spmetadatawebservicepartitiondata.md)
  
[Import-SPMetadataWebServicePartitionData](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/enterprise-content-management-cmdlets/import-spmetadatawebservicepartitiondata.md)

