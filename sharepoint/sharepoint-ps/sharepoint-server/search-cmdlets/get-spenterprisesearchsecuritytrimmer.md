---
title: "Get-SPEnterpriseSearchSecurityTrimmer"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 60fd124a-e678-4440-9e37-852372a6d977

description: "Returns a custom security trimmer."
---

# Get-SPEnterpriseSearchSecurityTrimmer

Returns a custom security trimmer.
  
```
Get-SPEnterpriseSearchSecurityTrimmer -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Identity <SecurityTrimmerPipeBind>]

```

## Example

------------------EXAMPLE------------------
  
```
Get-SPEnterpriseSearchServiceApplication -Identity MySSA | Get-SPEnterpriseSearchSecurityTrimmer
```

This example obtains the pluggable security trimmers registered in the search service application  `MySSA`.
  
## Detailed Description

This cmdlet returns the **SecurityTrimmer**. A custom security trimmer trims search results before the results are returned to the user. 
  
 If the **Identity** parameter is not specified, this cmdlet returns the security trimmer collection for the specified search application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the security trimmer.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name, for example, SearchApp1, or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SecurityTrimmerPipeBind  <br/> |Specifies the pluggable security trimmer used for the specified search application.  <br/> The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, or an instance of a valid **SecurityTrimmer** object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SecurityTrimmerPipeBind  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchSecurityTrimmer](new-spenterprisesearchsecuritytrimmer.md)
  
[Remove-SPEnterpriseSearchSecurityTrimmer](remove-spenterprisesearchsecuritytrimmer.md)

