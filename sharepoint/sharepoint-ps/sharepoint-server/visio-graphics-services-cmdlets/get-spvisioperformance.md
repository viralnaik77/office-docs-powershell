---
title: "Get-SPVisioPerformance"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 58ecfebc-a3ed-40d2-b886-af53e03f765c

description: "Returns the Visio Services settings for the performance of a Visio Services application."
---

# Get-SPVisioPerformance

Returns the Visio Services settings for the performance of a Visio Services application.
  
```
Get-SPVisioPerformance -VisioServiceApplication <SPVisioServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPVisioPerformance** cmdlet reads the service settings for managing and configuring peformance for a Visio Services application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> |Specifies the Visio Services application that contains the **SPVisioPerformance** object.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Visio Services application (for example, MyVisioService1); or an instance of a valid **SPVisioServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-----------------EXAMPLE---------------------- 
  
```
Get-SPVisioPerformance -VisioServiceApplication "VGS1"
```

This example gets settings related to performance for a Visio Services application.
  
## See also

#### 

[Set-SPVisioPerformance](set-spvisioperformance.md)

