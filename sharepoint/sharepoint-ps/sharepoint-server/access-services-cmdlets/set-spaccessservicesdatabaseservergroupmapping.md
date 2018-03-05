---
title: "Set-SPAccessServicesDatabaseServerGroupMapping"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a9c85dad-9bd5-48e0-9358-055ef544c33f

description: "Sets server group mappings."
---

# Set-SPAccessServicesDatabaseServerGroupMapping

Sets server group mappings.
  
```
Set-SPAccessServicesDatabaseServerGroupMapping [-ServiceContext] <SPServiceContextPipeBind> -DatabaseServerGroup <AccessServicesDatabaseServerGroupPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-CorporateCatalog <SwitchParameter>] [-DeveloperSite <SwitchParameter>] [-ObjectModel <SwitchParameter>] [-RemoteObjectModel <SwitchParameter>] [-StoreFront <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Set-SPAccessServicesDatabaseServerGroupMapping** cmdlet to set the mapping between the source of the request to create the application and the DatabaseServerGroup containing the server that is selected to create new databases on. Specify one or more of the sources to map them to the DatabaseServerGroup. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context to set.  <br/> |
|**ClearMapping** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Removes any existing mappings between the source of the creation and the DatabaseServerGroup.  <br/> |
|**DatabaseServerGroup** <br/> |Required  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerGroupPipeBind  <br/> |Specifies the database server group mapping to set.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**CorporateCatalog** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies Apps that are created from the App Catalog.  <br/> |
|**DeveloperSite** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies Apps that are created from the developer site.  <br/> |
|**ObjectModel** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies Apps that are created from the Object model.  <br/> |
|**RemoteObjectModel** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies Apps that are created from the client side object model.  <br/> |
|**StoreFront** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies Apps that are created from the SharePoint Store.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**ClearMapping** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DatabaseServerGroup** <br/> |Required  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabaseServerGroupPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**CorporateCatalog** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DeveloperSite** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ObjectModel** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**RemoteObjectModel** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**StoreFront** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------EXAMPLE----------
  
```
$context = [Microsoft.SharePoint.SPServiceContext]::GetContext($app.ServiceApplicationProxyGroup, [Microsoft.SharePoint.SPSiteSubscriptionIdentifier]::Default)
```

```
$dsg = Get-SPAccessServicesDatabaseServerGroup -ServiceContext $context
```

```
Set-SPAccessServicesDatabaseServerGroupMapping -ServiceContext $context -DatabaseServerGroup $dsg
```

This example sets a Access Services database server group mapping by using the  `$context` and  `$dsg` variables. 
  
## See also

#### 

[Get-SPAccessServicesDatabaseServerGroupMapping](get-spaccessservicesdatabaseservergroupmapping.md)

