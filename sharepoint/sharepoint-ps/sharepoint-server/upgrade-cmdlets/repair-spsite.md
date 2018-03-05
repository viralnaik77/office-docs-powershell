---
title: "Repair-SPSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ac3543b6-8726-4ef5-b70b-06c569f9b450

description: "Activates the RunRepairs method against the referenced SPSite object."
---

# Repair-SPSite

Activates the RunRepairs method against the referenced SPSite object.
  
```
Repair-SPSite [-Identity] <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-RuleId <Guid>] [-RunAlways <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Repair-SPSite** cmdlet runs one or all site collection health checks on the site collection and its contents. This cmdlet automatically repairs issues that it finds. 
  
Run the **Test-SPSite** cmdlet for reports of rules which were run and a summary of the results. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the URL or GUID of the site to run a repair.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**RuleId** <br/> |Optional  <br/> |System.Guid  <br/> |Specifies the specific site health rule to run instead of running all applicable rules at once.  <br/> |
|**RunAlways** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces a rule to run even if a health check was run.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

------------EXAMPLE 1--------------- 
  
```
Repair-SPSite http://<site name</sites/testsite
```

This example runs all the site collection health checks in repair mode on the http://\<site name\>/sites/testsite site collection.
  
------------EXAMPLE 2--------------- 
  
```
Repair-SPSite http://<site name>/sites/testsite -Rule "ee967197-ccbe-4c00-88e4-e6fab81145e1"
```

This example runs just the "Missing Galleries Check" in repair mode on the http://\<site name\>/sites/testsite site collection.
  
## See also

#### 

[Test-SPSite](test-spsite.md)

