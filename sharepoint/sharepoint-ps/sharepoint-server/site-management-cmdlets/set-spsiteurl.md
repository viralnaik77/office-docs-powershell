---
title: "Set-SPSiteUrl"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67e66f44-2522-4f00-aae5-5eb2db1aa90f

description: "Adds or changes an URL mapping for the site."
---

# Set-SPSiteUrl

Adds or changes an URL mapping for the site.
  
```
Set-SPSiteUrl [-Identity] <SPSitePipeBind> -Url <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]] [-Zone <Default | Intranet | Internet | Custom | Extranet>]
```

## Detailed Description

The **Set-SPSiteUrl** cmdlet adds or changes an URL mapping for the site. 
  
The **Set-SPSiteUrl** cmdlet only applies to the root site collection for a host name that is, http://www.contoso.com. This cmdlet cannot be directly run against a managed path site collection underneath the root that is, http://www.contoso.com/sites/test. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the URL or GUID of the site collection to set. Must be the root site collection for a host-name.  <br/> |
|**Url** <br/> |Required  <br/> |System.String  <br/> |Specifies the URL. This must be unique. This must be an absolute URL including scheme (that is, https://www.contoso.com). If URL exists, the current entry is updated. Otherwise, the URL entry is added and cannot be in use by another site collection.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> | Specifies one of the five zones with which the alternate URL is associated.  <br/>  The type must be any one of the following values:  <br/>  Default  <br/>  Intranet  <br/>  Internet  <br/>  Custom  <br/>  Extranet  <br/>  If the **Zone** parameter is not specified and is a new entry, the default value is set. If an entry exists and is not specified, do not change.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**Url** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> ||
   
## Example

---------------EXAMPLE------------ 
  
```
$site = Get-SPSite 'http://www.contoso.com'
```

```
Set-SPSiteURL -Identity $site -Url http://contoso.sharepoint.com -Zone Default

```

This example adds an additional URL, http://contoso.sharepoint.com, to the site collection. The newly added URL is in the default zone.
  
## See also

#### 

[Get-SPSiteUrl](get-spsiteurl.md)
  
[Remove-SPSiteUrl](remove-spsiteurl.md)

