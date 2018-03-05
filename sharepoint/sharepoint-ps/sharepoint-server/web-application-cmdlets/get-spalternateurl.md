---
title: "Get-SPAlternateURL"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea38119d-a535-48a3-b498-9daa443399fb

description: "Returns all alternate URLs that match a given set of criteria."
---

# Get-SPAlternateURL

Returns all alternate URLs that match a given set of criteria.
  
```
Get-SPAlternateURL [[-Identity] <SPAlternateUrlPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Zone <Default | Intranet | Internet | Custom | Extranet>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Get-SPAlternateURL** cmdlet returns all alternate URLs that match the scope given by either the optional **Identity** parameter or by a combination of the optional **WebApplication**, **Zone**, or **Resource** parameters. Each criterion that is added narrows the scope. If no criteria are specified then all alternate URLs are returned. 
  
If the **Identity** parameter is used, only the specific matching alternate URL is returned. If no alternate URL with the given identity exists at the given scope, nothing is returned. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAlternateUrlPipeBind  <br/> |Specifies the URL or GUID of the alternate URL to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh, or a valid URL, in the form http://server_name.  <br/> |
|**ResourceName** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the resource from which to list alternate URLs.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the Web application from which to list alternate URLs.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Zone** <br/> |Optional  <br/> |System.String  <br/> |Specifies one of the five zones with which the alternate URLs is associated.  <br/> Must be a valid zone: **Default**, **Intranet**, **Internet**, **Extranet**, or **Custom** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAlternateUrlPipeBind  <br/> ||
|**ResourceName** <br/> |Required  <br/> |System.String  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> ||
   
## Example

--------------EXAMPLE 1-----------------
  
```
Get-SPAlternateURL -WebApplication http://sitename
```

This example displays all the alternate URLs on a given Web application.
  
--------------EXAMPLE 2-----------------
  
```
Get-SPAlternateURL -ResourceName "MyResource"
```

This example displays all the alternate URLs for a given resource.
  
## See also

#### 

[New-SPAlternateUrl](new-spalternateurl.md)
  
[Set-SPAlternateUrl](set-spalternateurl.md)
  
[Remove-SPAlternateUrl](remove-spalternateurl.md)

