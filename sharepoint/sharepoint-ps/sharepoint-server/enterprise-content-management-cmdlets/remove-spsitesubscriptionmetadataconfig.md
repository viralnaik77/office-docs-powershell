---
title: "Remove-SPSiteSubscriptionMetadataConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6836e51d-35ff-454c-a755-bb36c70e4bc6

description: "Removes site subscription configuration settings."
---

# Remove-SPSiteSubscriptionMetadataConfig

Removes site subscription configuration settings.
  
```
Remove-SPSiteSubscriptionMetadataConfig [-Identity] <SPSiteSubscriptionPipeBind> [-ServiceProxy] <SPMetadataServiceProxyCmdletPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Remove-SPSiteSubscriptionMetadataConfig** cmdlet to remove the site subscription-specific configuration settings for a specified Metadata Service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site subscription for which to remove the Metadata Service application settings.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a site subscription (for example, SiteSubscriptionConfig1); or an instance of a valid **SiteSubscription** object.  <br/> |
|**ServiceProxy** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> |Specifies the local metadata service proxy for the service application containing the site subscription-specific settings.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of the service application proxy (for example, ServiceAppProxy1); or an instance of a valid **SPMetadataServiceProxy** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**ServiceProxy** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE-------------------
  
```
Remove-SPSiteSubscriptionMetadataConfig -Identity $siteSubscriptionPipeBind1 -ServiceProxy "MetadataServiceProxy2"
```

This example removes the site subscription-specific settings from an existing partitioned Metadata Service application.
  
## See also

#### 

[Set-SPSiteSubscriptionMetadataConfig](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/set-spsitesubscriptionmetadataconfig.md)
  
[Get-SPSiteSubscriptionMetadataConfig](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/get-spsitesubscriptionmetadataconfig.md)

