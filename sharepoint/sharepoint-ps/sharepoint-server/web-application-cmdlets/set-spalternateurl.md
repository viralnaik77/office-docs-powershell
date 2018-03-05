---
title: "Set-SPAlternateUrl"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 846b5eb0-f235-4970-837b-f8f2657722a9

description: "Configures the specified alternate URL."
---

# Set-SPAlternateUrl

Configures the specified alternate URL.
  
```
Set-SPAlternateUrl [-Identity] <SPAlternateUrlPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Url <String>] [-WhatIf [<SwitchParameter>]] [-Zone <Default | Intranet | Internet | Custom | Extranet>]
```

## Detailed Description

The **Set-SPAlternateUrl** cmdlet changes the URL or zone of the alternate URL specified by the **Identity** parameter. This cmdlet can be used to change only the zone of internal URLs, and cannot be used to change the zone of public URLs. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPAlternateUrlPipeBind  <br/> |Specifies the URL or GUID of the alternate URL to change.  <br/> The type must be a valid URL, in the form http://server_name/WebApplication/site, or a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**Url** <br/> |Optional  <br/> |System.String  <br/> |Specifies the new alternate URL.  <br/> |
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> |Sets the supplied alternate URL as one of the five zones.  <br/> The type must be any one of the following values: **Default**, **Intranet**, **Internet**, **Extranet**, or **Custom**.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPAlternateUrlPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Url** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> ||
   
## Example

------------------EXAMPLE 1------------------
  
```
Set-SPAlternateURL -Identity https://www.contoso.com -Zone "Internet"
```

This example changes the zone of the alternate URL  `https://www.contoso.com`.
  
------------------EXAMPLE 2------------------
  
```
Set-SPAlternateURL -Identity https://www.contoso.com -Url https://sharepoint.contoso.com -Zone "Default"
```

This example changes the URL and zone of the alternate URL  `https://www.contoso.com`.
  
------------------EXAMPLE 3------------------
  
```
Get-SPAlternateURL https://www.contoso.com | Set-SPAlternateURL -Zone "Internet"
```

This example changes the zone of the alternate URL  `https://www.contoso.com`.
  
------------------EXAMPLE 4------------------
  
```
Get-SPWebApplication |%{ Get-SPAlternateURL -WebApplication $_ -Zone "Extranet" } | Set-SPAlternateURL -Zone "Intranet"
```

This example changes the zone of the alternate URL for the specified Web application from  `Extranet` to  `Intranet`.
  
## See also

#### 

[Get-SPAlternateURL](get-spalternateurl.md)
  
[New-SPAlternateUrl](new-spalternateurl.md)
  
[Remove-SPAlternateUrl](remove-spalternateurl.md)

