---
title: "Set-SPContentDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: e1de8a07-868e-4a0d-bb5b-1f62392523f8

description: "Sets global properties of a SharePoint content database."
---

# Set-SPContentDatabase

Sets global properties of a SharePoint content database.
  
```
Set-SPContentDatabase -Identity <SPContentDatabasePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DatabaseFailoverServer <String>] [-MaxSiteCount <Int32>] [-Status <Online | Disabled | Offline | Unprovisioning | Provisioning | Upgrading | Patching>] [-WarningSiteCount <Int32>] [-WhatIf [<SwitchParameter>]]

```

## Example

---------------EXAMPLE 1---------------
  
```
Get-SPContentDatabase http://contoso.com | Set-SPContentDatabase -MaxSiteCount 1
```

This example sets the  `MaxSiteCount` for the content database that contains  `contoso.com` to  `1`.
  
---------------EXAMPLE 2---------------
  
```
Get-SPContentDatabase -WebApplication http://sitename | Set-SPContentDatabase -WarningSiteCount $null
```

This example clears the  `WarningSiteCount` for all databases in the  `sitename` Web application. 
  
## Detailed Description

The **Set-SPContentDatabase** cmdlet sets global properties of a SharePoint content database. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the content database to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint content database (for example, SPContentDB1); or an instance of a valid **SPContentDatabase** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _DatabaseFailoverServer_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the mirror server for failover.  <br/> |
| _MaxSiteCount_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the maximum number of site collections that this database can host.  <br/> The type must be a positive integer. Set to $null to clear this value.  <br/> |
| _Status_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPObjectStatus  <br/> | Specifies the status of the SQL Server database. Set this parameter to **Online** to make the database available to host new sites. Set this parameter to **Offline** to make the database unavailable to host new sites.  <br/>  The valid values must be either of the following:  <br/> **Online** <br/> **Offline** <br/> **Disabled** <br/> **Unprovisioning** <br/> **Provisioning** <br/> **Upgrading** <br/> **Patching** <br/> |
| _WarningSiteCount_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of site collections that can be created before a warning event is generated and the owner of the site collection is notified.  <br/> The type must be a positive integer. Set to $null to clear this value.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**MaxSiteCount** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Status** <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPObjectStatus  <br/> ||
|**WarningSiteCount** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPContentDatabase](get-spcontentdatabase.md)
  
[Upgrade-SPContentDatabase](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/upgrade-cmdlets/upgrade-spcontentdatabase.md)
  
[Dismount-SPContentDatabase](dismount-spcontentdatabase.md)
  
[Test-SPContentDatabase](test-spcontentdatabase.md)
#### 

[New-SPContentDatabase](http://technet.microsoft.com/library/18cf18cd-8fb7-4561-be71-41c767f27b51.aspx)
  
[Remove-SPContentDatabase](http://technet.microsoft.com/library/e8c337b6-37af-4fdd-8469-a32f4d45c040.aspx)

