---
title: "Update-SPFarmEncryptionKey"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2cde77eb-0bb8-4047-9333-aa915f11a390

description: "Changes the value of the farm encryption key and, using the new key, re-encrypts all the data."
---

# Update-SPFarmEncryptionKey

Changes the value of the farm encryption key and, using the new key, re-encrypts all the data.
  
```
Update-SPFarmEncryptionKey [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Resume <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Update-SPFarmEncryptionKey** cmdlet changes the farm encryption key to a new randomly generated value. When the new key is used, all the data is re-encrypted. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Resume** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Resumes re-encryption of data with the new farm encryption key if a previous attempt failed.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

------------------EXAMPLE-----------------------
  
```
Update-SPFarmEncryptionKey -confirm
```

This example changes the farm encryption key to a new value and re-encrypts all the data.
  

