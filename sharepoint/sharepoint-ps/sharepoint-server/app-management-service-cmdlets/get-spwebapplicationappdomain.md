---
title: "Get-SPWebApplicationAppDomain"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/8/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: df3e0051-745d-472b-abe1-8356d4a7c6ae

description: "Returns all app domains for a specific web application."
---

# Get-SPWebApplicationAppDomain

Returns all app domains for a specific web application. 
  
```
Get-SPWebApplicationAppDomain [[-Identity] <SPAppDomainPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Zone <Default | Intranet | Internet | Custom | Extranet>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Get-SPWebApplicationAppDoman** cmdlet to return all app domains for a specific web application or for all web applications. If you do not specify parameters, the default zone is used. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPAppCmdlets.SPAppDomainPipeBind  <br/> |Specifies the string of a domain name (that is, contoso.com) or a **SPAppDomain** object.  <br/> |
|**AppDomain** <br/> |Required  <br/> |System.String  <br/> |Specifies the URI of the app domain.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the GUID, URI, or name of the web application for which the app domain is being configured.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> | Specifies the security zone to which the app domain will be assigned.  <br/>  Default  <br/>  Intranet  <br/>  Internet  <br/>  Extranet  <br/>  Custom  <br/>  If no value is specified, Default is applied.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPAppCmdlets.SPAppDomainPipeBind  <br/> ||
|**AppDomain** <br/> |Required  <br/> |System.String  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> ||
   
## Example

-----------EXAMPLE 1--------- 
  
```
Get-SPWebApplicationAppDomain
```

Returns a list of **SPAppDomain** objects, one for each of the app domains for all web applications in the farm. 
  
-----------EXAMPLE 2--------- 
  
```
Get-SPWebApplicationAppDomain -Zone Default
```

Returns a list of **SPAppDomain** objects, one for each of the app domains for the Default zone for all web applications in the farm. 
  
-----------EXAMPLE 3--------- 
  
```
Get-SPWebApplicationAppDomain -WebApplication http://www.contoso.com

```

Returns a list of **SPAppDomain** objects, one for each of all the app domains for the specified web application for all zones. 
  
-----------EXAMPLE 4--------- 
  
```
Get-SPWebApplicationAppDomain -AppDomain contosoapps.com
```

Returns a list of **SPAppDomain** objects, one for each web application and zone pair that shares the specified app domain. 
  
## See also

#### 

[New-SPWebApplicationAppDomain](new-spwebapplicationappdomain.md)
  
[Remove-SPWebApplicationAppDomain](remove-spwebapplicationappdomain.md)

