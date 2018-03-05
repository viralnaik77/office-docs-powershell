---
title: "Set-SPServer"
ms.author: kirks
author: Techwriter40
ms.date: 9/13/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0892c859-c209-40eb-b10c-3686aee28eea

description: "Changes the role of the server."
---

# Set-SPServer

Changes the role of the server.
  
```
Set-SPServer -Identity <SPServerPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Role <Invalid | WebFrontEnd | Application | SingleServer | SingleServerFarm | DistributedCache | Search | Custom | ApplicationWithSearch | WebFrontEndWithDistributedCache>] [-Status <Online | Disabled | Offline | Unprovisioning | Provisioning | Upgrading | Patching>]

```

## Example

--------------EXAMPLE 1-----------------
  
```
Set-SPServer -Role SingleServerFarm
```

This example changes the server to SingleServerFarm role.
  
## Detailed Description

The **Set-SPServer** cmdlet changes the role of the server in the farm by using the **Role** parameter. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServerPipeBind  <br/> |Specifies the name of the server in the farm.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Role_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPServerRole  <br/> | Specifies the name of the server role you want to change.  <br/>  The valid values are:  <br/>  WebFrontEnd  <br/>  Application  <br/>  SingleServerFarm  <br/>  Distributed Cache  <br/>  Search  <br/>  Custom  <br/>  ApplicationWithSearch  <br/>  WebFrontEndWithDistributedCache  <br/> > [!NOTE]>  The **Custom** and **SingleServerFarm** roles require manually maintenance by the farm administrator.           |
| _Status_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPObjectStatus  <br/> |Sets the status of the server in the farm.  <br/> |
   
## See also

#### 

[Get-SPServer](get-spserver.md)
  
[Rename-SPServer](rename-spserver.md)
#### 

[Upgrade-SPServer](http://technet.microsoft.com/library/2b29cab3-296e-424e-a7d6-5b213be30aad.aspx)

