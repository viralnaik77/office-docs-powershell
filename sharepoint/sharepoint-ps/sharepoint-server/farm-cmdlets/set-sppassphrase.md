---
title: "Set-SPPassPhrase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13a76a78-fed5-4148-9fcb-df81d1514be8

description: "Sets the pass phrase to a new value."
---

# Set-SPPassPhrase

Sets the pass phrase to a new value.
  
```
Set-SPPassPhrase -ConfirmPassPhrase <SecureString> -PassPhrase <SecureString> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
The **Set-SPPassPhrase** cmdlet sets the Passphrase to a new Passphrase value. If the **LocalServerOnly** parameter is not used, the farm encryption key is re-encrypted with the new value and attempts to propagate this value to all other servers in the farm. If the **LocalServerOnly** parameter is used, this is updated on the local machine only, and the farm encryption key is not changed. The Passphrase value must be the same on all servers in the farm if the farm is to function correctly. So if the Passphrase fails to propagate to all servers, the **LocalServerOnly** parameter can be used to set the remaining servers to the new Passphrase value manually. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ConfirmPassphrase** <br/> |Required  <br/> |System.Security.SecureString  <br/> |Passphrase is typed a second time to confirm that it matches the first entry.  <br/> |
|**Passphrase** <br/> |Required  <br/> |System.SecuritySecureString  <br/> |Specifies the new Passphrase value.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**LocalServerOnly** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Scopes the Passphrase change to the local server only. If this parameter is not used, the Passphrase change is performed farm-wide.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ConfirmPassPhrase** <br/> |Required  <br/> |System.Security.SecureString  <br/> ||
|**PassPhrase** <br/> |Required  <br/> |System.Security.SecureString  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**LocalServerOnly** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
$passphrase=ConvertTo-SecureString -asPlainText -Force
```

```
Set-SPPassPhrase -PassPhrase $passphrase -Confirm
```

This example queries for a string to use as a  `passphrase`, and sets the farm passphrase to a new value.
  

