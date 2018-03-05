---
title: "Remove-SPWebApplicationAppDomain"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/8/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 377b6a82-1ba1-422d-b7a2-c906389f7ce1

description: "Deletes the AppDomain."
---

# Remove-SPWebApplicationAppDomain

Deletes the AppDomain.
  
```
Remove-SPWebApplicationAppDomain [-Identity] <SPAppDomainPipeBind> -WebApplication <SPWebApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]][-Zone <Default | Intranet | Internet | Custom | Extranet>]
```

## Detailed Description

Use the **Remove-SPWebApplicationAppDomain** cmdlet to delete the AppDomain for a specified zone or to delete all the app domains for the web application if no zone is specified. 
  
> [!NOTE]
> This cmdlet also deletes the Internet Information Services (IIS) port binding if any was added for the WebApp/Zone combination. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppCmdlets.SPAppDomainPipeBind  <br/> |Specifies the string of a domain name (that is, contoso.com) or a **SPAppDomain** object to remove.  <br/> |
|**WebApplication** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the GUID, URI, or name of the web application for which the app domain is being removed.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Zone** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPUrlZone  <br/> | Specifies the security zone to which the app domain will be assigned.  <br/>  Default  <br/>  Intranet  <br/>  Internet  <br/>  Extranet  <br/>  Custom  <br/>  If no value is specified, Default is applied.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppCmdlets.SPAppDomainPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

---------------EXAMPLE 1-------------- 
  
```
Remove-SPWebApplicationAppDomain -WebApplication http://www.contoso.com

```

Removes all of the app domains for the specified web application.
  
---------------EXAMPLE 2-------------- 
  
```
Remove-SPWebApplicationAppDomain -WebApplication http://www.contoso.com -Zone Internet
```

Removes the app domains for the internet zone for the specified web application.
  
## See also

#### 

[Get-SPWebApplicationAppDomain](get-spwebapplicationappdomain.md)
  
[New-SPWebApplicationAppDomain](new-spwebapplicationappdomain.md)

