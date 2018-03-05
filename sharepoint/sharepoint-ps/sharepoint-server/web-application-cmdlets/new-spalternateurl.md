---
title: "New-SPAlternateUrl"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 450f057d-1cb8-4680-b28d-0db4d1b7e09c

description: "Creates a new public or internal URL for the specified Web application zone or resource."
---

# New-SPAlternateUrl

Creates a new public or internal URL for the specified Web application zone or resource.
  
```
New-SPAlternateUrl [-Url] <String> -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Internal <SwitchParameter>] [-WhatIf [<SwitchParameter>]] [-Zone <Default | Intranet | Internet | Custom | Extranet>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **New-SPAlternateUrl** cmdlet creates a new public or internal URL for the specified Web application zone or resource. Use the **ResourceName** parameter if the alternate URL is for an external resource. 
  
Each Web application can be associated with a collection of mappings between internal and public URLs. Both internal and public URLs consist of the protocol and domain portion of the full URL; for example, https://www.fabrikam.com. Users type a public URL to get to the SharePoint site, and that URL appears in the links on the pages. Internal URLs are in the URL requests that are sent to the SharePoint site. Many internal URLs can be associated with a single public URL in multiserver farms; for example, when a load balancer routes requests to specific IP addresses to various servers in the load-balancing cluster.
  
Each Web application supports five collections of mappings per URL; the five collections correspond to five zones (default, intranet, extranet, Internet, and custom). When the Web application receives a request for an internal URL in a particular zone, links on the pages returned to the user have the public URL for that zone.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Url** <br/> |Required  <br/> |System.String  <br/> |Specifies the public URL that users access to sign in to the Web application.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the name, URL, or GUID of the Web application for which to create the mapping.  <br/> The type must be a valid name, URL, in the form WebApplication-1212, http://server_name, or GUID, in the form 1234-5678-9876-0987.  <br/> |
|**ResourceName** <br/> |Required  <br/> |System.String  <br/> |Specifies the resource name, if the alternate URL is for an external resource. If no value is specified, the value is left blank.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Internal** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Makes this alternate URL an internal URL. If this parameter is not provided, the URL is a public URL.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Zone** <br/> |Optional  <br/> |System.String  <br/> |Specifies one of the five zones with which the alternate URL is associated.  <br/> The type must be a valid zone: **Default**, **Intranet**, **Internet**, **Extranet**, or **Custom**.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Url** <br/> |Required  <br/> |System.String  <br/> ||
|**ResourceName** <br/> |Required  <br/> |System.String  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Internal** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
#create the public URLNew-SPAlternateURL https://www.contoso.com -Zone "Internet"
```

```
#create the internal URLNew-SPAlternateURL http://sharepoint.contoso.com -Zone "Internet" -internal
```

This example translates incoming requests for  `https://www.contoso.com` into  `http://sharepoint.contoso.com` (on the  `Internet` zone). 
  
When a reverse proxy is being set up to handle public URL SSL termination, alternate access mappings must be configured to handle the URL translation.
  
## See also

#### 

[Set-SPAlternateUrl](set-spalternateurl.md)
  
[Get-SPAlternateURL](get-spalternateurl.md)
  
[Remove-SPAlternateUrl](remove-spalternateurl.md)

