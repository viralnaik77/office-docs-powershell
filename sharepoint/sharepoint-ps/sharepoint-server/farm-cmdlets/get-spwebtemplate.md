---
title: "Get-SPWebTemplate"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfd10bac-c304-4f3f-bea9-eb0af5f96df5

description: "Displays all globally installed site templates that match the given identity."
---

# Get-SPWebTemplate

Displays all globally installed site templates that match the given identity.
  
```
Get-SPWebTemplate [[-Identity] <SPWebTemplatePipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <UInt32>]
```

## Detailed Description

The **Get-SPWebTemplate** cmdlet displays all installed site templates that match the full or partial identity that was given. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the name of the Web template to display.  <br/> The type must be the ID or full or partial name of the Web template.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**CompatibilityLevel** <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the version of templates to use when creating a new SPSite object. This value sets the initial CompatibilityLevel value for the site collection. The values for this parameter can be either SharePoint Server 2010 or SharePoint Server 2016. When this parameter is not specified, the CompatibilityLevel will default to the highest possible version for the Web application depending on the SiteCreationMode setting  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebTemplatePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**CompatibilityLevel** <br/> |Optional  <br/> |System.UInt32  <br/> ||
   
## Example

--------------EXAMPLE 1-----------------
  
```
$template = Get-SPWebTemplate "STS#0"
```

```
New-SPSite http://contoso.com -OwnerAlias "DOMAIN\JDOE" -Template $template
```

This example creates a site collection by using the team site Web template (ID= `STS#0`).
  
--------------EXAMPLE 2-----------------
  
```
Get-SPWebTemplate "STS*"
```

This example displays basic information about all the  `STS` templates. 
  

