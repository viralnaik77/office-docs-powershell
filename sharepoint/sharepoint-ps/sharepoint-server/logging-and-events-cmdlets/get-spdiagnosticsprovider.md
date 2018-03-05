---
title: "Get-SPDiagnosticsProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f5b4243-3a83-4c83-b301-f8f5bb737b48

description: "Returns a diagnostics provider."
---

# Get-SPDiagnosticsProvider

Returns a diagnostics provider.
  
```
Get-SPDiagnosticsProvider [[-Identity] <SPDiagnosticsProviderPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Get-SPDiagnosticsProvider** cmdlet reads the specified diagnostics provider. If the **Identity** parameter is not specified, this cmdlet returns the collection diagnostics providers in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPDiagnosticsProviderPipeBind  <br/> |Specifies the diagnostics provider to get.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a diagnostic provider (for example, DiagnosticsProv1); or an instance of a valid **SPDiagnosticsProvider** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPDiagnosticsProviderPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Get-SPDiagnosticsProvider
```

This example returns all the diagnostics providers in the farm.
  
------------------EXAMPLE 2-----------------------
  
```
Get-SPDiagnosticsProvider job-diagnostics-event-log-provider
```

This example returns the event log diagnostics provider.
  
## See also

#### 

[Set-SPDiagnosticsProvider](set-spdiagnosticsprovider.md)

