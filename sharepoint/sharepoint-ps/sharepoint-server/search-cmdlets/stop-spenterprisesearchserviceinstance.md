---
title: "Stop-SPEnterpriseSearchServiceInstance"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 985591b0-951f-4274-aead-a184398bba41

description: "Stops an instance of a search service."
---

# Stop-SPEnterpriseSearchServiceInstance

Stops an instance of a search service.
  
```
Stop-SPEnterpriseSearchServiceInstance -Identity <SearchServiceInstancePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
Get-SPEnterpriseSearchServiceInstance -Local | Stop-SPEnterpriseSearchServiceInstance
```

This example stops the local search service instance.
  
## Detailed Description

This cmdlet stops an instance of a search service.
  
> [!NOTE]
> Before you can stop a search service instance, you must remove all search topology components on the associated server from the active topology. This can be done in three ways: > - Removing components from the search topology. If there are items in the search index, see [Manage search components in SharePoint Server 2013](http://technet.microsoft.com/library/197ce911-c4f6-40a3-84c1-fb5999623b51.aspx) and [Manage the index component in SharePoint Server 2013](http://technet.microsoft.com/library/6c4f87aa-1004-4b87-aaca-2c262588fc46.aspx). If there are no items in the search index, see [Change the default search topology in SharePoint Server 2013](http://technet.microsoft.com/library/7fa9730a-2d11-4c78-b546-60179c5bb646.aspx). > - Moving components to another server. If there are items in the search index, see [Manage search components in SharePoint Server 2013](http://technet.microsoft.com/library/197ce911-c4f6-40a3-84c1-fb5999623b51.aspx) and [Manage the index component in SharePoint Server 2013](http://technet.microsoft.com/library/6c4f87aa-1004-4b87-aaca-2c262588fc46.aspx). If there are no items in the search index, see [Change the default search topology in SharePoint Server 2013](http://technet.microsoft.com/library/7fa9730a-2d11-4c78-b546-60179c5bb646.aspx). > - Removing the search service application. For more information, see [Remove-SPEnterpriseSearchServiceApplication](remove-spenterprisesearchserviceapplication.md)
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> |Specifies the shared search service instance to stop.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a query server (for example, MyQueryServer); or an instance of a valid **SearchServiceInstance** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchServiceInstance](get-spenterprisesearchserviceinstance.md)
  
[Start-SPEnterpriseSearchServiceInstance](start-spenterprisesearchserviceinstance.md)

