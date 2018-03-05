---
title: "Test-SPSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4941af13-fcb0-4747-86b0-e43ab9b39090

description: "Activates the RunTests method against a referenced SPSite object."
---

# Test-SPSite

Activates the RunTests method against a referenced SPSite object.
  
```
Test-SPSite [-Identity] <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-RuleId <Guid>] [-RunAlways <SwitchParameter>]
```

## Detailed Description

The **Test-SPSite** cmdlet runs one or all site collection health checks on the site collection and its contents. This cmdlet reports the rules which were run and provides a summary of the results. 
  
To run tests in repair mode, use the **Repair-SPSite** cmdlet. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies the URL or GUID of the site to run a test.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**RuleId** <br/> |Optional  <br/> |System.Guid  <br/> |Specifies one specific site health rule to run.  <br/> |
|**RunAlways** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces a rule to run even if a health check was run.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**RuleId** <br/> |Optional  <br/> |System.Guid  <br/> ||
|**RunAlways** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

--------------EXAMPLE 1------------ 
  
```
Test-SPSite http://<site name>/sites/testsite
```

This example runs all the site collection health checks on the http://\<site name\>/sites/testsite site collection.
  
--------------EXAMPLE 2------------ 
  
```
Test-SPSite http://<site name</sites/testsite -Rule "ee967197-ccbe-4c00-88e4-e6fab81145e1"
```

This example runs just the "Missing Galleries Check" on the http://\<site name\>/sites/testsite site collection.
  
## See also

#### 

[Repair-SPSite](repair-spsite.md)

