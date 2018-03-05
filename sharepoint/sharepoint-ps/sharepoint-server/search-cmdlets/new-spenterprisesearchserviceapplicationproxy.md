---
title: "New-SPEnterpriseSearchServiceApplicationProxy"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2a074a5a-0af0-48fd-aa1f-edc875f93335

description: "Adds a new search application proxy to a farm."
---

# New-SPEnterpriseSearchServiceApplicationProxy

Adds a new search application proxy to a farm.
  
```
New-SPEnterpriseSearchServiceApplicationProxy -Uri <String> <COMMON PARAMETERS>

```

## Example

-----------------EXAMPLE 1------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "My_SSA_Name"

```

```
$SSAProxy = New-SPEnterpriseSearchServiceApplicationProxy -name "My_SSA_Proxy" -Uri $ssa.Uri.AbsoluteURI

```

In this example, we create a proxy for a search service application by specifying the URI to the search service application.
  
In the first line, we use the **Get-SPEnterpriseSearchServiceApplication** cmdlet to retrieve the search service application we want to create a proxy for. In the example, the search service application has the name "My_SSA_Name". If you don't specify the search service application to retrieve, and the farm has multiple search service applications, the **Get-SPEnterpriseSearchServiceApplication** cmdlet returns a list of all search service applications on the farm. This causes the proxy creation in the second line to fail. 
  
In the second line, we use the **New-SPEnterpriseSearchServiceApplication** cmdlet to create a proxy named "My_SSA_Proxy" for the search service application named "My_SSA_Name". Because we specify the URI to the search service application, the cmdlet uses the first parameter set. The first parameter set doesn't require us to specify the search service application object. 
  
-----------------EXAMPLE 2------------------
  
```
$ssa = Get-SPEnterpriseSearchServiceApplication -Identity "My_SSA_Name"

```

```
$SSAProxy = New-SPEnterpriseSearchServiceApplicationProxy -name "My_SSA_Proxy" -SearchApplication $ssa

```

In this example, we create a proxy for a search service application by specifying the search service application object.
  
In the first line, we use the **Get-SPEnterpriseSearchServiceApplication** cmdlet to retrieve the search service application object that we want to create a proxy for. In the example, the search service application has the name "My_SSA_Name". 
  
In the second line, we use the **New-SPEnterpriseSearchServiceApplication** cmdlet to create a proxy named "My_SSA_Proxy" for the search service application named "My_SSA_Name". Because we specify the search service application object, the cmdlet uses the second parameter set. The second parameter set doesn't require us to specify the URI to the search service application. 
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
This cmdlet creates a proxy for a single search service application. Via the proxy, a web application or another service consumer can use the functionality the search application provides.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application to create a proxy for.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name; or a valid **SearchServiceApplication** object.  <br/> > [!NOTE]> If you specify this parameter, you aren't required to specify the **Uri** parameter.           |
| _Uri_ <br/> |Required  <br/> |System.String  <br/> |Specifies the URI of the search service application to create a proxy for.  <br/> The type must be a valid URI of an endpoint address. The endpoint address is available from the search service application object, in the form $ssa.Uri.AbsoluteUri.  <br/> > [!NOTE]> If you specify this parameter, you aren't required to specify the **SearchApplication** parameter.           |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _MergeWithDefaultPartition_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Merges the index partition for the proxy with the default index partition collection for the search service application.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the display name of the search application proxy to create.  <br/> The type must be a valid string, for example, SearchAppProxy1.  <br/> |
| _Partitioned_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the search service application must use web-hosted mode. Web-hosted mode segregates results for a given hosted subscription.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**Uri** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**MergeWithDefaultPartition** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Partitioned** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchServiceApplicationProxy](get-spenterprisesearchserviceapplicationproxy.md)
  
[Set-SPEnterpriseSearchServiceApplicationProxy](set-spenterprisesearchserviceapplicationproxy.md)
  
[Remove-SPEnterpriseSearchServiceApplicationProxy](remove-spenterprisesearchserviceapplicationproxy.md)

