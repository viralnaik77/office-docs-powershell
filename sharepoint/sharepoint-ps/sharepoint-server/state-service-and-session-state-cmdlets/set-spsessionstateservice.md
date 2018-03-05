---
title: "Set-SPSessionStateService"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86b546f7-1d16-4ab6-bfa8-90402b1ea043

description: "Updates the credentials that are used to communicate with the state service database."
---

# Set-SPSessionStateService

Updates the credentials that are used to communicate with the state service database.
  
```
Set-SPSessionStateService [-DatabaseCredentials <PSCredential>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SessionTimeout <Int32>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------------EXAMPLE-----------------
  
```
Set-SPSessionStateService -SessionTimeout 120
```

This example changes the ASP.NET session state time-out to 2 hours.
  
## Detailed Description

The **Set-SPSessionStateService** cmdlet updates the credentials that are used to communicate with the state service database. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseCredentials_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the database credentials for SQL Authentication that are used to access the state service database. If this parameter is not specified, Windows authentication is used.  <br/> The type must be a valid **PSCredential** object.  <br/> |
| _SessionTimeout_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the time, in minutes that an ASP.NET session will remain active with no user activity.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseCredentials** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**SessionTimeout** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Disable-SPSessionStateService](disable-spsessionstateservice.md)
  
[Enable-SPSessionStateService](enable-spsessionstateservice.md)
  
[Get-SPSessionStateService](get-spsessionstateservice.md)

