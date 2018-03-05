---
title: "Get-SPAccessServicesDatabase"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/20/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e85c2fd7-13b5-42a7-ba57-ce58f3b77189

description: "Returns an Access Services database or a collection of Access Services databases."
---

# Get-SPAccessServicesDatabase

Returns an Access Services database or a collection of Access Services databases.
  
```
Get-SPAccessServicesDatabase [-AccessAppsOnly <$true | $false>] [-AssignmentCollection <SPAssignmentCollection>] [-ContentDb <SPContentDatabasePipeBind>] [-Identity <AccessServicesDatabasePipeBind>]

```

## Example

---------EXAMPLE----------
  
```
$asdbs = Get-SPAccessServicesDatabase | select-object -property Url,DatabaseName,DatabaseServer;
```

This example returns Access Services databases in the farm that display the Url, DatabaseName, and DatabaseServer properties.
  
## Detailed Description

Use the **Get-SPAccessServicesDatabase** cmdlet to return an Access Services database. If the **Identity** parameter is not specified, the cmdlet returns the collection of Access Services databases that are in the Web service application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AccessAppsOnly_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies to return only Access applications.  <br/> The default value is true.  <br/>  If the value is to false SharePoint applications, will be returned, not just Access.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _ContentDb_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the SharePoint content database.  <br/> |
| _Identity_ <br/> |Optional  <br/> |Microsoft.Office.Access.Services.PowerShell.AccessServicesDatabasePipeBind  <br/> |Specifies the Access Services Database to return.  <br/> |
   

