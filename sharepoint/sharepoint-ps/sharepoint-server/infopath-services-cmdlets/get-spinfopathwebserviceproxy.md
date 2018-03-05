---
title: "Get-SPInfoPathWebServiceProxy"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d55b41b1-9743-4438-9dae-fe4dde896e7a

description: "Returns the Web proxy settings for the Web application."
---

# Get-SPInfoPathWebServiceProxy

Returns the Web proxy settings for the Web application.
  
```
Get-SPInfoPathWebServiceProxy [-Identity] <SPWebServiceProxyPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPInfoPathWebServiceProxy** cmdlet reads the Web proxy settings for the SharePoint Web application specified in **Identity**. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPWebServiceProxyPipeBind  <br/> |Specifies the SharePoint Web application to get.  <br/> The type must be a valid URL, in the form http://server_name, or a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.InfoPath.Server.Cmdlet.SPWebServiceProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

--------------EXAMPLE-----------------
  
```
Get-SPInfoPathWebServiceProxy -Identity "http://server_name"
```

This example displays the Web service proxy settings for a specified Web application.
  
## See also

#### 

[Set-SPInfoPathWebServiceProxy](set-spinfopathwebserviceproxy.md)

