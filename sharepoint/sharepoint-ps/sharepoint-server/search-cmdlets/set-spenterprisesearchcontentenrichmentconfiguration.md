---
title: "Set-SPEnterpriseSearchContentEnrichmentConfiguration"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7d803d1c-0b1d-4205-acdb-75d2878b6cfe

description: "Stores the specified content enrichment configuration to the Search service application."
---

# Set-SPEnterpriseSearchContentEnrichmentConfiguration

Stores the specified content enrichment configuration to the Search service application.
  
```
Set-SPEnterpriseSearchContentEnrichmentConfiguration -ContentEnrichmentConfiguration <ContentEnrichmentConfigurationPipeBind> -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE 1 ------------------ 
  
```
$config = New-SPEnterpriseSearchContentEnrichmentConfiguration$config.Endpoint = "http://server/service"$config.InputProperties = "Title", "Url"$config.OutputProperties = "Title", "Url"$ssa = Get-SPEnterpriseSearchServiceApplicationSet-SPEnterpriseSearchContentEnrichmentConfiguration -SearchApplication $ssa -ContentEnrichmentConfiguration $config
```

This example creates a new **ContentEnrichmentConfiguration** object. The URL of the external web service is stored in the  `$config.Endpoint` property. The new **ContentEnrichmentConfiguration** is configured to use  `Title` and  `URL`, which are the managed properties that you want to send to the external web service. It is also configured to expect the external web service to output the same managed properties. The **SearchServiceApplication** object is retrieved, and used for storing the newly created **ContentEnrichmentConfiguration**. 
  
------------------EXAMPLE 2 ------------------ 
  
```
$config = New-SPEnterpriseSearchContentEnrichmentConfiguration
```

```
$config.Endpoint = "http://server/service"$config.InputProperties = "Title"$config.OutputProperties = "Title"$config.Trigger = 'Contains(Title, "Example")'
```

```
$ssa = Get-SPEnterpriseSearchServiceApplication

```

```
Set-SPEnterpriseSearchContentEnrichmentConfiguration -SearchApplication $ssa -ContentEnrichmentConfiguration $config
```

This example creates a new **ContentEnrichmentConfiguration** object. The URL of the external web service is stored in the  `$config.Endpoint` property. The new **ContentEnrichmentConfiguration** is configured to use  `Title`, which is the managed property that you want to send to the external web service. It is also configured to expect the external web service to output the same managed property. The  `$config.Trigger` is set to only send the managed property when the Boolean trigger expression is true, in this case when the managed property Title contains the string  `"Example".` The **SearchServiceApplication** object is retrieved, and used for storing the newly created **ContentEnrichmentConfiguration**. 
  
## Detailed Description

This cmdlet validates the **ContentEntrichmentConfiguration** object and stores the provided configuration in the **SearchServiceApplication**. Both a **ContentEnrichmentConfiguration** and a **SearchServiceApplication** object have to be provided. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ContentEnrichmentConfiguration_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.PipeBind.ContentEnrichmentConfigurationPipeBind  <br/> |Specifies the **ContentEnrichmentConfiguration** that should be stored in the **SearchServiceApplication**.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the **SearchServiceApplication** that contains the **ContentEnrichmentConfiguration**.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ContentEnrichmentConfiguration** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.PipeBind.ContentEnrichmentConfigurationPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchContentEnrichmentConfiguration](get-spenterprisesearchcontentenrichmentconfiguration.md)
  
[New-SPEnterpriseSearchContentEnrichmentConfiguration](new-spenterprisesearchcontentenrichmentconfiguration.md)
  
[Remove-SPEnterpriseSearchContentEnrichmentConfiguration](remove-spenterprisesearchcontentenrichmentconfiguration.md)

