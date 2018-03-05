---
title: "New-SPSecureStoreApplicationField"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1735293f-628a-409b-afb9-a10b5399dbd3

description: "Creates a new Secure Store application fields object."
---

# New-SPSecureStoreApplicationField

Creates a new Secure Store application fields object.
  
```
New-SPSecureStoreApplicationField -Masked <SwitchParameter> -Name <String> -Type <UserName | Password | Pin | Key | Generic | WindowsUserName | WindowsPassword | Certificate | CertificatePassword> [-AssignmentCollection <SPAssignmentCollection>]

```

## Detailed Description

The **New-SPSecureStoreApplicationField** cmdlet creates a new Secure Store application field object for a target application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Masked** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Masks the visible characters that are typed in the field.  <br/> |
|**Name** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the new target application field.  <br/> |
|**Type** <br/> |Required  <br/> |Microsoft.BusinessData.Infrastructure.SecureStore.SecureStoreCredentialType  <br/> |Specifies the type of credential field to add to a target application.  <br/> The type must be one of the following: **UserName**, **Password**, **Pin**, **Key**, **Generic**, **WindowsUserName**, or **WindowsPassword**.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Masked** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**Type** <br/> |Required  <br/> |Microsoft.BusinessData.Infrastructure.SecureStore.SecureStoreCredentialType  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
New-SPSecureStoreApplicationField -Name "UserName" -Type WindowsUserName -Masked:$false
```

This example creates a new credential field of type  `WindowsUserName` with the name  `UserName`, and the masked property (which when true will hide characters as they are typed in by the user) set to  `false`. This cmdlet is typically used in conjunction with the **New-SPSecureStoreApplication** cmdlet. 
  
## See also

#### 

[New-SPSecureStoreTargetApplication](new-spsecurestoretargetapplication.md)
  
[New-SPSecureStoreApplication](new-spsecurestoreapplication.md)

