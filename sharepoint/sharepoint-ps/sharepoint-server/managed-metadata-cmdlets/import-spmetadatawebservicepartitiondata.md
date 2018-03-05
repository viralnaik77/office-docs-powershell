---
title: "Import-SPMetadataWebServicePartitionData"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 15b11931-a9e7-43a7-adb3-8399b1c0cc7c

description: "Restores the data for a site subscription."
---

# Import-SPMetadataWebServicePartitionData

Restores the data for a site subscription.
  
```
Import-SPMetadataWebServicePartitionData -Identity <SPSiteSubscriptionPipeBind> -Path <String> -ServiceProxy <SPMetadataServiceProxyCmdletPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-NoCompression <SwitchParameter>] [-OverwriteExisting <SwitchParameter>] [-ToContentDatabase <SPContentDatabasePipeBind>] [-ToServiceDatabase <SwitchParameter>]

```

## Example

-------------------EXAMPLE----------------------
  
```
Import-SPMetadataWebServicePartitionData -Identity $siteSubscriptionPipeBind1 -ServiceProxy "MetadataServiceProxy2" -Path "\\server_name\folder_name\file_name.cab"
```

This example restores a backup of Metadata Service application data for a specific site subscription on a Metadata Service application.
  
## Detailed Description

Use the **Import-SPMetadataWebServicePartitionData** cmdlet to restore data for a site subscription to a shared service application for the Metadata Service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site subscription to import.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a site subscription (for example, SiteSubscriptionConfig1); or an instance of a valid **SiteSubscription** object.  <br/> |
| _Path_ <br/> |Required  <br/> |System.String  <br/> |Specifies the path and name of the subscription data file to import.  <br/> The type must be a valid path in either of the following forms:  <br/> -  _C:\folder_name\formtemplate_name_ <br/> -  _\\server_name\folder_name\file_name.cab_ <br/> |
| _ServiceProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> |Specifies the proxy for the service application that contains the site subscription.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of the service application proxy (for example, ServiceAppProxy1); or an instance of a valid **SPMetadataServiceProxy** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _NoCompression_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |PARAMVALUE: SwitchParameter  <br/> |
| _OverwriteExisting_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to overwrite the existing site subscription data, if it exists.  <br/> |
| _ToContentDatabase_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |PARAMVALUE: SPContentDatabasePipeBind  <br/> |
| _ToServiceDatabase_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |PARAMVALUE: SwitchParameter  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**ServiceProxy** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> ||
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**OverwriteExisting** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Clear-SPMetadataWebServicePartitionData](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/enterprise-content-management-cmdlets/clear-spmetadatawebservicepartitiondata.md)
  
[Export-SPMetadataWebServicePartitionData](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/enterprise-content-management-cmdlets/export-spmetadatawebservicepartitiondata.md)

