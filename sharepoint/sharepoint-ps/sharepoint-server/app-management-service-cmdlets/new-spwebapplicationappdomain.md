---
title: "New-SPWebApplicationAppDomain"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/8/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 892ab687-3f59-4e22-9ade-e8c6e1163609

description: "Creates an AppDomain entry."
---

# New-SPWebApplicationAppDomain

Creates an AppDomain entry.
  
```
New-SPWebApplicationAppDomain [-AppDomain] <String> -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Port <Int32>] [-SecureSocketsLayer <SwitchParameter>] [-WhatIf [<SwitchParameter>]] [-Zone <Default | Intranet | Internet | Custom | Extranet>]
```

## Detailed Description

Use the **New-SPWebApplicationAppDomain** cmdlet to create an AppDomain entry. If you specify a port, the cmdlet adds a port binding to the Internet Information Services (IIS) site corresponding to the webapp/ zone combination. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppDomain** <br/> |Required  <br/> |System.String  <br/> |Specifies the URI of the app domain.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the GUID, URI, or name of the web application for which the app domain is being configured.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Port** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the IIS port number to which the app domain will be assigned. If no value is specified, the same port used by the web application for the zone is applied.  <br/> |
|**SecureSocketsLayer** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies that the app domain will use Secured Sockets Layer (SSL) security. If no value is specified, no SSL security will be used.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> | Specifies the security zone to which the app domain will be assigned.  <br/>  Default  <br/>  Intranet  <br/>  Internet  <br/>  Extranet  <br/>  Custom  <br/>  If no value is specified, Default is applied.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppDomain** <br/> |Required  <br/> |System.String  <br/> ||
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Port** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**SecureSocketsLayer** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> ||
   
## Example

----------EXAMPLE 1------------ 
  
```
New-SPWebApplicationAppDomain -AppDomain contosoapps.com -WebApplication http://www.contoso.com
```

Creates a new app domain for apps for SharePoint for the specified web application in the default zone.
  
----------EXAMPLE 2------------ 
  
```
New-SPWebApplicationAppDomain -AppDomain contosoapps.com -WebApplication http://www.contoso.com -Zone Internet -Port 10000
```

Creates a new app domain for apps for SharePoint for the specified web application in the internet zone at port 10000.
  
## See also

#### 

[Get-SPWebApplicationAppDomain](get-spwebapplicationappdomain.md)
  
[Remove-SPWebApplicationAppDomain](remove-spwebapplicationappdomain.md)

