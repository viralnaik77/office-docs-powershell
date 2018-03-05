---
title: "Set-SPSiteSubscriptionMetadataConfig"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d6d174ed-6534-4ea9-8aa0-b93c87c6c5d7

description: "Sets the site subscription configuration settings for a specified Metadata Service application."
---

# Set-SPSiteSubscriptionMetadataConfig

Sets the site subscription configuration settings for a specified Metadata Service application.
  
```
Set-SPSiteSubscriptionMetadataConfig [-Identity] <SPSiteSubscriptionPipeBind> [-ServiceProxy] <SPMetadataServiceProxyCmdletPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DoNotUnpublishAllPackages <SwitchParameter>] [-HubUri <String>] [-SyndicationErrorReportEnabled <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPSiteSubscriptionMetadataConfig** cmdlet to set the site subscription-specific settings for a specified shared service application for the Metadata Service. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the site subscription for which to set the Metadata Service application settings.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a site subscription (for example, SiteSubscriptionConfig1); or an instance of a valid **SiteSubscription** object.  <br/> |
|**ServiceProxy** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> |Specifies the local metadata service proxy for the service application that contains the site subscription-specific settings.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of the service application proxy (for example, ServiceAppProxy1); or an instance of a valid **SPMetadataServiceProxy** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DoNotUnpublishAllPackages** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**HubUri** <br/> |Optional  <br/> |System.String  <br/> |Specifies the URI of the syndication hub.  <br/> The type must be a valid URI, in the form file:\\server_name\sitedocs.  <br/> |
|**SyndicationErrorReportEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables error reporting for content type syndication.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**ServiceProxy** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DoNotUnpublishAllPackages** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**HubUri** <br/> |Optional  <br/> |System.String  <br/> ||
|**SyndicationErrorReportEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------------EXAMPLE---------------------
  
```
Set-SPSiteSubscriptionMetadataConfig -Identity $siteSubscriptionPipeBind1 -ServiceProxy "MetadataServiceProxy2" -HubUri "http://sitename" -SyndicationErrorReportEnabled:$false
```

This example sets the content type syndication hub and disables syndication error reporting for a specific site subscription on an existing partitioned Metadata Service application.
  
## See also

#### 

[Remove-SPSiteSubscriptionMetadataConfig](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/remove-spsitesubscriptionmetadataconfig.md)
  
[Get-SPSiteSubscriptionMetadataConfig](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/get-spsitesubscriptionmetadataconfig.md)

