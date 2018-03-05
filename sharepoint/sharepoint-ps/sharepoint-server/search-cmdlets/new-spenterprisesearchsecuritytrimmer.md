---
title: "New-SPEnterpriseSearchSecurityTrimmer"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 493d9d19-ae43-43ce-b75f-916535881b35

description: "Adds a custom security trimmer to a shared search application."
---

# New-SPEnterpriseSearchSecurityTrimmer

Adds a custom security trimmer to a shared search application.
  
```
New-SPEnterpriseSearchSecurityTrimmer -Id <Int32> -SearchApplication <SearchServiceApplicationPipeBind> -TypeName <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Properties <String>] [-RulePath <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication

```

```
New-SPEnterpriseSearchSecurityTrimmer -SearchApplication $searchapp -TypeName "SearchCustomSecurityTrimmer.CustomSecurityTrimmerPost, SearchCustomSecurityTrimmer, Version=1.0.0.0, Culture=neutral, PublicKeyToken=48e046c834625a88, processorArchitecture=MSIL" -Id 1
```

This example adds a new custom security trimmer for trimming the returned result set. This new security trimmer is added to the search application by using the id  `1`. The strong named assembly contains the class  `CustomSecurityTrimmerPost`, which implements the ISecurityTrimmerPost interface. 
  
## Detailed Description

This cmdlet creates a new object to configure the security trimmer. **SPEnterpriseSearchSecurityTrimmer** represents a security trimmer that performs customized security trimming of search results at query time, when the results are returned to the user. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Id_ <br/> |Required  <br/> |System.Int32  <br/> |Specifies the identity of the security trimmer to use for the specified search application. If this parameter specifies an existing custom security trimmer, the trimmer will be removed and replaced with the custom trimmer. Remove the existing trimmer before you add a new one.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Adds the security trimmer to the specified search application.  <br/> The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _TypeName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the strong named assembly name of a security trimmer type. The strong name must refer to a type whose assembly is deployed to the global assembly cache on a query server, and that type must implement the **ISecurityTrimmerPre**, **ISecurityTrimmerPost** or **ISecurityTrimmer2** interface. Security trimming can be done in two places: before query execution (ISecurityTrimmerPre) or after the results set has returned (ISecurityTrimmerPost or ISecurityTrimmer2). For how to reference a strong name assembly, see [https://msdn.microsoft.com/en-us/library/s1sx4kfb.aspx](https://msdn.microsoft.com/en-us/library/s1sx4kfb.aspx) <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Properties_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name-value pairs that specify the configuration properties.  <br/> The type must be in the following name/value pair format: Name1~Value1~Name2~Value2~  <br/> |
| _RulePath_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the content path where the security trimmer will be applied.  <br/> The string must be a valid URI in the form file:\\server_name\content, and it must correspond to an existing crawl rule.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Id** <br/> |Required  <br/> |System.Int32  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**TypeName** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Properties** <br/> |Optional  <br/> |System.String  <br/> ||
|**RulePath** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchSecurityTrimmer](get-spenterprisesearchsecuritytrimmer.md)
  
[Remove-SPEnterpriseSearchSecurityTrimmer](remove-spenterprisesearchsecuritytrimmer.md)

