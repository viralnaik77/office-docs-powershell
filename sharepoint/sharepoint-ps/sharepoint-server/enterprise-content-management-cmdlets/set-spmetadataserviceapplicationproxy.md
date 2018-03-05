---
title: "Set-SPMetadataServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fc5ea28-a67d-4fc0-895d-164b92ad8247

description: "Sets the properties of a connection to a managed metadata service application."
---

# Set-SPMetadataServiceApplicationProxy

Sets the properties of a connection to a managed metadata service application.
  
```
Set-SPMetadataServiceApplicationProxy [-Identity] <SPMetadataServiceProxyCmdletPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ContentTypePushdownEnabled <SwitchParameter>] [-ContentTypeSyndicationEnabled <SwitchParameter>] [-DefaultKeywordTaxonomy <SwitchParameter>] [-DefaultProxyGroup <SwitchParameter>] [-DefaultSiteCollectionTaxonomy <SwitchParameter>] [-Name <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPMetadataServiceApplicationProxy** cmdlet to set the properties of a connection to a managed metadata service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> |Specifies the connection to update.  <br/> The type must be a GUID that represents the identity of the connection to modify, the name of a valid connection to a managed metadata service, or an instance of a valid **SPMetadataServiceProxy** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**ContentTypePushdownEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that existing instances of changed content types in subsites and libraries will be updated.  <br/> |
|**ContentTypeSyndicationEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that this connection will provide access to the content types that are associated with the managed metadata service application.  <br/> |
|**DefaultKeywordTaxonomy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that new enterprise keywords will be stored in the term store associated with the managed metadata service application.  <br/> > [!NOTE]>  Do not make more than one connection the default keyword location.           |
|**DefaultSiteCollectionTaxonomy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the term set that is created when you create a new managed metadata column will be stored in the term store associated with the managed metadata service application.  <br/> > [!NOTE]> Do not make more than one connection the default location for site collection term sets.           |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the new display name of the connection. The name can contain a maximum of 128 characters.  <br/> |
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the connection be added to the default proxy group of the farm.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceProxyCmdletPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ContentTypePushdownEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ContentTypeSyndicationEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultKeywordTaxonomy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultSiteCollectionTaxonomy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------------EXAMPLE 1---------------------
  
```
Set-SPMetadataServiceApplicationProxy -Identity "MetadataServiceProxy1" -ContentTypeSyndicationEnabled -ContentTypePushdownEnabled
```

This example enables content type syndication and enables content type pushdown on an existing connection to a managed metadata service application.
  
-----------------EXAMPLE 2---------------------
  
```
Set-SPMetadataServiceApplicationProxy -Identity "MetadataServiceProxy1" -ContentTypeSyndicationEnabled:$false -ContentTypePushdownEnabled:$false
```

This example disables content type syndication and disables content type pushdown on an existing connection to a managed metadata service application.
  
-----------------EXAMPLE 3---------------------
  
```
Set-SPMetadataServiceApplicationProxy -Identity "MetadataServiceProxy1" -DefaultKeywordTaxonomy -DefaultSiteCollectionTaxonomy:$false
```

This example configures an existing connection to a managed metadata service application to be the default location for storing enterprise keywords and prevents it from being the default location for storing column-specific term sets.
  
## See also

#### 

[Get-SPMetadataServiceApplicationProxy](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/get-spmetadataserviceapplicationproxy.md)
  
[New-SPMetadataServiceApplicationProxy](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/new-spmetadataserviceapplicationproxy.md)

