---
title: "New-SPManagedAccount"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a863892f-5bf5-4e6f-b35e-8f31be2a41c4

description: "Registers a new managed account."
---

# New-SPManagedAccount

Registers a new managed account.
  
```
New-SPManagedAccount [-Credential] <PSCredential> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **New-SPManagedAccount** cmdlet registers a new managed account for the specified **Credential** or **Username**, and **Password**. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Credential** <br/> |Required  <br/> |System.Management.Automation.PSCredential  <br/> |Indicates the **Credential** object that specifies the credentials of the new managed account. If you use **Credential**, you cannot specify **Username** and **Password**.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

------------------EXAMPLE-----------------------
  
```
$cred = Get-Credential
```

```
New-SPManagedAccount -Credential $cred
```

This example adds a new managed account to the farm by using credentials that are prompted.
  
## See also

#### 

[Get-SPManagedAccount](get-spmanagedaccount.md)
  
[Set-SPManagedAccount](set-spmanagedaccount.md)
  
[Remove-SPManagedAccount](remove-spmanagedaccount.md)

