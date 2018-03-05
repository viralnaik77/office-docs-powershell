---
title: "Add-SPUserLicenseMapping"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 94befda8-5390-4569-a566-21ceb690618f

description: "Maps a security group, forms-based role, or claim to a SharePoint user license."
---

# Add-SPUserLicenseMapping

Maps a security group, forms-based role, or claim to a SharePoint user license.
  
```
Add-SPUserLicenseMapping -Mapping <List> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Add-SPUserLicenseMapping** cmdlet maps a claim, Active Directory Domain Services (AD DS) security group, or forms-based role to a SharePoint user license for a farm or web application. To specify a mapping to a specific web application, use the WebApplication parameter. If you do not specify parameters, mapping applies to the entire SharePoint farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Mapping** <br/> |Required  <br/> |System.Collections.Generic.List  <br/> |Specifies a mapping to use. For example, an Active Directory security group.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

---------------EXAMPLE 1-------------------
  
```
$a = New-SPUserLicenseMapping -SecurityGroup yoursecuritygroup -License Enterprise
```

```
Add-SPUserLicenseMapping -Mapping $a
```

This example adds user mappings for the entire farm.
  
## See also

#### 

[Disable-SPUserLicensing](disable-spuserlicensing.md)
  
[Enable-SPUserLicensing](enable-spuserlicensing.md)
  
[Get-SPUserLicenseMapping](get-spuserlicensemapping.md)
  
[Remove-SPUserLicenseMapping](remove-spuserlicensemapping.md)

