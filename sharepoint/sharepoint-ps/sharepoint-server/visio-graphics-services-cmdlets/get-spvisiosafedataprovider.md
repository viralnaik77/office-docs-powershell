---
title: "Get-SPVisioSafeDataProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 05711a37-cde6-437d-a6b6-16128cfdc580

description: "Returns the settings of a safe data provider for a Visio Services application."
---

# Get-SPVisioSafeDataProvider

Returns the settings of a safe data provider for a Visio Services application.
  
```
Get-SPVisioSafeDataProvider -VisioServiceApplication <SPVisioServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-DataProviderId <String>] [-DataProviderType <Int32>]
```

## Detailed Description

The **Get-SPVisioSafeDataProvider** cmdlet retrieves the settings of the safe provider for a Visio Services application. If the **DataProviderID** parameter is not specified, this cmdlet returns the collection of safe providers in the farm. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> |Specifies the Visio Services application that contains the **SPVisioSafeDataProvider** object.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Visio Services application (for example, MyVisioService1); or an instance of a valid **SPVisioServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**DataProviderId** <br/> |Optional  <br/> |System.String  <br/> |Specifies the safe data provider to get. The combination of **DataProviderID** and **DataProviderType** uniquely identify a data provider for a Visio Graphics Service application. The string that identifies the data provider can be a maximum of 255 alphanumeric characters.  <br/> The type must be a valid string that identifies the data provider; for example, VisioDataProvider1.  <br/> |
|**DataProviderType** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the supported type of the data provider to get. Custom data types are supported; for example, Excel services.  <br/> The type must be a valid identity of a data provider type.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**DataProviderId** <br/> |Optional  <br/> |System.String  <br/> ||
|**DataProviderType** <br/> |Optional  <br/> |System.Int32  <br/> ||
   
## Example

-------------------EXAMPLE 1----------------------
  
```
Get-SPVisioSafeDataProvider -VisioServiceApplication "VGS1"
```

This example returns a list of safe data providers for a specific Visio Services application.
  
-------------------EXAMPLE 2----------------------
  
```
Get-SPVisioSafeDataProvider -VisioServiceApplication "VGS1" -DataProviderID "SQLOLEDB" -DataProviderType 1
```

This example returns information about a specified safe data provider for a specific Visio Services application.
  
## See also

#### 

[New-SPVisioSafeDataProvider](new-spvisiosafedataprovider.md)
  
[Remove-SPVisioSafeDataProvider](remove-spvisiosafedataprovider.md)
  
[Set-SPVisioSafeDataProvider](set-spvisiosafedataprovider.md)

