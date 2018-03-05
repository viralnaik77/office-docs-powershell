---
title: "Get-SPInfoPathUserAgent"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fef7e923-ac38-4054-aa7b-cd1f143d487e

description: "Returns a user agent or all the currently defined user agents for the farm."
---

# Get-SPInfoPathUserAgent

Returns a user agent or all the currently defined user agents for the farm.
  
```
Get-SPInfoPathUserAgent [[-Identity] <SPUserAgentPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPInfoPathUserAgent** cmdlet reads the user agent specified in **Identity**. If the **Identity** parameter is not specified, this cmdlet returns the collection of user agents for the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPUserAgentPipeBind  <br/> |Specifies the user agent to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a user agent (for example, UserAgent1; or an instance of a valid **SPUserAgent** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPUserAgentPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPInfoPathUserAgent
```

This example displays a list of user agents in the entire farm.
  
## See also

#### 

[Add-SPInfoPathUserAgent](add-spinfopathuseragent.md)
  
[Remove-SPInfoPathUserAgent](remove-spinfopathuseragent.md)

