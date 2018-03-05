---
title: "Get-SPFeature"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f00cddab-fc38-42fb-8bb7-c9aec2e99a28

description: "Returns the SharePoint Features based on a given criteria."
---

# Get-SPFeature

Returns the SharePoint Features based on a given criteria.
  
```
Get-SPFeature [[-Identity] <SPFeatureDefinitionPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Limit <String>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
All parameter sets take the **Identity** parameter, which can be either the relative path of the SharePoint Feature (considered the feature name) or the GUID of a Feature definition. If the **Identity** parameter is provided, the cmdlets attempt to find the given Feature definition or instance for the given scope. If no parameters are specified, all installed features are returned. 
  
The **Get-SPFeature** cmdlet behaves differently at each scope, returning the enabled Features at each level. If no scope is provided, all installed Features are returned. 
  
> [!NOTE]
> The names returned by the **Get-SPFeature** cmdlet are different that the names displayed in the SharePoint Central Administration website. An example of hot to find a specific feature by name is provided in the examples section of this article. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPFeatureDefinitionPipeBind  <br/> |Specifies the name of the Feature to retrieve.  <br/> The type must be the full or partial name, in the form Feature1, or a GUID, in the form 1234-4567-9879, of the Feature to get .  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Farm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that if this parameter is used, only enabled farm Features are displayed.  <br/> |
|**Limit** <br/> |Optional  <br/> |System.String  <br/> |Limits the display results. If "All" is specified, all Features are displayed.  <br/> The type must be a valid number greater than 0. The default value is 200.  <br/> |
|**Site** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the name of the site collection from which to get enabled Features.  <br/> The type must be a valid URL for a site collection, in the form http://server_name .  <br/> |
|**Web** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebPipeBind  <br/> |Specifies the URL or GUID of the Web.  <br/> The type must be a valid URL, in the form http://server_name , or a GUID, in the form 1234-5678-9876-0987.  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the name of the Web application from which to get enabled Features.  <br/> The type must be a valid URL to the Web application in the form http://server_name .  <br/> |
|**CompatibilityLevel** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the version of templates to use when creating a new **SPSite** object. This value sets the initial CompatibilityLevel value for the site collection. When this parameter is not specified, the CompatibilityLevel will default to the highest possible version for the web application depending on the CompatibilityRange setting.  <br/> |
   
## Example

--------------EXAMPLE 1-----------------
  
```
Get-SPFeature -Limit ALL | Where-Object {$_.Scope -eq "SITE"}
```

This example returns a list of all installed  `SITE` scoped Features. 
  
--------------EXAMPLE 2-----------------
  
```
Get-SPFeature -Limit ALL | Where-Object {$_.DisplayName -like "*Access*"}
```

This example returns the features that have  `Access` in their **DisplayName**.
  
--------------EXAMPLE 3-----------------
  
```
Get-SPSite http://somesite | Get-SPWeb -Limit ALL | Where-Object { Get-SPFeature -Web $_ } | Select DisplayName,ID -Unique
```

This example returns the name and identifier (ID) of each uniquely enabled Feature on every **SPWeb** object in the site collection at  `http://somesite`.
  
## See also

#### 

[Install-SPFeature](install-spfeature.md)
  
[Enable-SPFeature](enable-spfeature.md)
  
[Disable-SPFeature](disable-spfeature.md)
  
[Uninstall-SPFeature](uninstall-spfeature.md)

