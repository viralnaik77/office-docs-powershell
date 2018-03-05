---
title: "New-SPUserLicenseMapping"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 2/23/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 08add796-78f3-4287-af29-0e0ec3eec8f4

description: "Creates a license mapping object."
---

# New-SPUserLicenseMapping

Creates a license mapping object.
  
```
New-SPUserLicenseMapping -License <String> -SecurityGroup <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WebApplication <SPWebApplicationPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **New-SPUserLicenseMapping** cmdlet to create a new license mapping object. This cmdlet must be used first before the **Add-SPUserLicenseMapping** cmdlet can be used. 
  
The object created by using the **New-SPUserLicenseMapping** cmdlet is stored in memory and is not written to any database in SharePoint Server 2016. After the object is created you can pipe the result to the **Add-SPUserLicenseMapping** cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Claim** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim  <br/> |Specifies the claims principal to license. The value must be an authentic claims principal.  <br/> |
|**ClaimType** <br/> |Required  <br/> |System.String  <br/> |Specifies the type of the claim. The value must be an authentic name of a claim type.  <br/> |
|**License** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of a supported SharePoint user license. For the full list of supported licenses on a SharePoint farm, see the [Get-SPUserLicense](get-spuserlicense.md) cmdlet.  <br/> |
|**OriginalIssuer** <br/> |Required  <br/> |System.String  <br/> |Specifies the original issuer of the claim. The value must be the authentic name of an original issuer.  <br/> |
|**Role** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of a forms-based role. The value must be an authentic name of a forms-based role.  <br/> |
|**RoleProviderName** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of a role provider. The value must be an authentic name of a role provider.  <br/> |
|**SecurityGroup** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of an AD DS security group. The value must be a name of an Active Directory security group.  <br/> |
|**Value** <br/> |Required  <br/> |System.String  <br/> |Specifies the value of the claim. The value must be an authentic claim value.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**ValueType** <br/> |Optional  <br/> |System.String  <br/> |Specifies the value type of the claim. The value must be an authentic name of a claim value type.  <br/> |
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the URL, GUID, web application name, or web application object instance where the mapping is to be added. If you omit this parameter, the mapping is applied to the entire farm.  <br/> The type must be an URL in the form http://server_name or http://server_name/sites/sitename, a GUID (for example, 12345678-90ab-cdef-1234-567890bcdefgh), a name of a web application (for example, SharePoint - 80), or an instance of a web application object.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Claim** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.Claims.SPClaim  <br/> ||
|**ClaimType** <br/> |Required  <br/> |System.String  <br/> ||
|**License** <br/> |Required  <br/> |System.String  <br/> ||
|**OriginalIssuer** <br/> |Required  <br/> |System.String  <br/> ||
|**Role** <br/> |Required  <br/> |System.String  <br/> ||
|**RoleProviderName** <br/> |Required  <br/> |System.String  <br/> ||
|**SecurityGroup** <br/> |Required  <br/> |System.String  <br/> ||
|**Value** <br/> |Required  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ValueType** <br/> |Optional  <br/> |System.String  <br/> ||
|**WebApplication** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

----------EXAMPLE-------------
  
```
$a=New-SPUserLicenseMapping -SecurityGroup yoursecuritygroup -License Enterprise
```

```
$a | Add-SPUserLicenseMapping
```

This example creates a license mapping object and then pipes the result to the Add-SPUserLicenseMapping cmdlet.
  
## See also

#### 

[Add-SPUserLicenseMapping](add-spuserlicensemapping.md)
  
[Get-SPUserLicenseMapping](get-spuserlicensemapping.md)
  
[Remove-SPUserLicenseMapping](remove-spuserlicensemapping.md)

