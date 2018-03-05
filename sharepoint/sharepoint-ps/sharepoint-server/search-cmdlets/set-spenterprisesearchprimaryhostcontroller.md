---
title: "Set-SPEnterpriseSearchPrimaryHostController"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 05f14b40-f1dd-4b6f-a015-f764587d38f5

description: "Applies to: UNRESOLVED_TOKEN_VAL(zzpub_appliesTo)"
---

# Set-SPEnterpriseSearchPrimaryHostController

 * **Applies to: ** UNRESOLVED_TOKEN_VAL(zzpub_appliesTo) * 
  
Sets the primary search host controller for the farm.
  
```
Set-SPEnterpriseSearchPrimaryHostController -SearchServiceInstance <SearchServiceInstancePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE 1------------------
  
```
$ssi = Get-SPEnterpriseSearchServiceInstance -Local 
Set-SPEnterpriseSearchPrimaryHostController $ssi
```

This example sets the local **SearchHostController** instance as the new primary **SearchHostController**. It is up to the user to select the **HostController** with latest version available. If you choose a SearchHostController that is not running the latest version of the repository, you will have to confirm before you continue. 
  
------------------EXAMPLE 2------------------
  
```
$ssi = Get-SPEnterpriseSearchServiceInstance -Local 
Set-SPEnterpriseSearchPrimaryHostController $ssi -Force
```

This example sets the local **SearchHostController** instance as the new primary **SearchHostController**. If you choose a **SearchHostController** that is not running the latest version of the repository, you will  *not*  get a confirmation message before you continue. 
  
## Detailed Description

This cmdlet sets the primary **SearchHostController** for the farm to the defined **SearchHostController**. 
  
The SearchHostController is related to the SearchServiceInstance, where the SearchHostController manages the search components that run on a server, and maintains a local repository for linguistic dictionaries. The search components retrieve the linguistic dictionaries from the PrimaryHostController.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchServiceInstance_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> |**SearchServiceInstance** of the server from where the **SearchHostController** object is returned.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Force_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Force the change of the primary **SearcHostController**. No confirmation messages are asked, even if user tries to set primary to a **SearchHostController** not running the latest version of the repository.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchServiceInstance** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceInstancePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchServiceInstance](get-spenterprisesearchserviceinstance.md)

