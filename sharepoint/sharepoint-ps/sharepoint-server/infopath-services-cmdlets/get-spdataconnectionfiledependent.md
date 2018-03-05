---
title: "Get-SPDataConnectionFileDependent"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 41cb3e6e-aedd-47dd-945b-a72b800013a6

description: "Returns deployed forms on the server dependent on a universal data connection."
---

# Get-SPDataConnectionFileDependent

Returns deployed forms on the server dependent on a universal data connection.
  
```
Get-SPDataConnectionFileDependent [-Identity] <SPDataConnectionFilePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPDataConnectionFileDependent** returns all administrator deployed forms that depend on a specified universal data connection (.udc) file located in the central data connection store. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPDataConnectionFilePipeBind  <br/> |Specifies the data connection file to get.  <br/> The type must be a valid GUID, in form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a data connection file (for example, DataConnectionFileName1.udcx); or an instance of a valid **SPDataConnectionFile** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPDataConnectionFilePipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPDataConnectionFileDependant -Identity "FileName.udcx
```

```
"FileName.udcx" | Get-SPDataConnectionFileDependant
```

This example displays a list of deployed forms with a specified name.
  

