---
title: "New-SPMetadataServiceApplicationProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e2c96d7d-d443-4457-8348-16d0a84e0b8e

description: "Creates a new connection to a managed metadata service application."
---

# New-SPMetadataServiceApplicationProxy

Creates a new connection to a managed metadata service application.
  
```
New-SPMetadataServiceApplicationProxy -Name <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-ContentTypePushdownEnabled <SwitchParameter>] [-ContentTypeSyndicationEnabled <SwitchParameter>] [-DefaultKeywordTaxonomy <SwitchParameter>] [-DefaultProxyGroup <SwitchParameter>] [-DefaultSiteCollectionTaxonomy <SwitchParameter>] [-PartitionMode <SwitchParameter>] [-ServiceApplication <SPMetadataServiceCmdletPipeBind>] [-Uri <String>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **New-SPMetadataServiceApplicationProxy** cmdlet to create a new connection to a managed metadata service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the display name of the service application proxy to create. The name can contain a maximum of 128 characters.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**ContentTypePushdownEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that existing instances of changed content types in subsites and libraries will be updated.  <br/> |
|**ContentTypeSyndicationEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that this connection will provide access to the content types that are associated with the managed metadata service application.  <br/> |
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the connection be added to the default proxy group for the farm.  <br/> |
|**DefaultKeywordTaxonomy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that new enterprise keywords will be stored in the term store associated with the managed metadata service application.  <br/> |
|**DefaultSiteCollectionTaxonomy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the term set that is created when you create a new managed metadata column will be stored in the term store associated with the managed metadata application.  <br/> |
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the service application restrict data by subscription.  <br/> > [!NOTE]> This property cannot be changed after the service application proxy has been created.           |
|**ServiceApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceCmdletPipeBind  <br/> |Specifies the local managed metadata service application to connect to. The service application must exist on the local farm.  <br/> The type must be a valid GUID; a valid name of the service application; or an instance of a valid **SPMetadataServiceApplication** object.  <br/> |
|**Uri** <br/> |Optional  <br/> |System.String  <br/> |Specifies the URI of a remote managed metadata service application to connect to.  <br/> > [!NOTE]> To specify the managed metadata service application that this proxy is connecting to, you must set only the **URI** parameter or only the **ServiceApplication** parameter.           The type must be a valid URL, in the form urn:schemas-microsoft-com:sharepoint:service:fa5c65ebed244a15817768825004f3a7#authority=urn:uuid:acdd6deff6sd4bb899f5beb42051bf3b7&amp;authority=https://  _\<server\>_:32844/Topology/topology.svc.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ContentTypePushdownEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ContentTypeSyndicationEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultKeywordTaxonomy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultProxyGroup** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DefaultSiteCollectionTaxonomy** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ServiceApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.Taxonomy.Cmdlet.SPMetadataServiceCmdletPipeBind  <br/> ||
|**Uri** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-------------------EXAMPLE 1----------------
  
```
New-SPMetadataServiceApplicationProxy -Name "MetadataServiceProxy1" -ServiceApplication "MetadataServiceApp1"
```

This example creates a connection to a managed metadata service application in the local farm.
  
-------------------EXAMPLE 2----------------
  
```
New-SPMetadataServiceApplicationProxy -Name "MetadataServiceProxy3" -ServiceApplication "MetadataServiceApp3" -PartitionMode
```

This example creates a partitioned connection to a managed metadata service application in the local farm.
  
## See also

#### 

[Get-SPMetadataServiceApplicationProxy](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/get-spmetadataserviceapplicationproxy.md)
  
[Set-SPMetadataServiceApplicationProxy](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/set-spmetadataserviceapplicationproxy.md)

