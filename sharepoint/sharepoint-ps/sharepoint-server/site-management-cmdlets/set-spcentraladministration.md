---
title: "Set-SPCentralAdministration"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/16/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a8bf87b6-18e6-4ba0-ada9-91ee9f4199ec

description: "Sets the port for the SharePoint Central Administration web site."
---

# Set-SPCentralAdministration

Sets the port for the SharePoint Central Administration web site. 
  
```
Set-SPCentralAdministration -Port <Int32> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-SecureSocketsLayer <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
Set-SPCentralAdministration -Port 3000
```

This example sets the Central Administration site on the local farm to HTTP port 3000.
  
------------------EXAMPLE 2-----------------------
  
```
Set-SPCentralAdministration -Port 3000 -SecureSocketsLayer
```

This example sets the Central Administration site on the local farm to SSL port 3000.
  
## Detailed Description

The **Set-SPCentralAdministration** cmdlet sets the port for the Central Administration web site. This affects all servers that are running the Central administration web site in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Port_ <br/> |Required  <br/> |System.Int32  <br/> |Specifies the administration port for the Central Administration site.  <br/> The type must be a valid port number; for example, 8080.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _SecureSocketsLayer_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables Secure Socket Layer (SSL) encryption for the specified port. If you choose to use SSL, you must assign a server certificate to the Central Administration IIS web site by using the IIS administration tools. The Central Administration web application won't be accessible until you do this.  <br/> The default value is **False**.  <br/> > [!NOTE]> If this parameter is omitted or set to False the Central Administration site will use HTTP for the specified port.           |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[New-SPCentralAdministration](new-spcentraladministration.md)
  
[Remove-SPCentralAdministration](remove-spcentraladministration.md)

