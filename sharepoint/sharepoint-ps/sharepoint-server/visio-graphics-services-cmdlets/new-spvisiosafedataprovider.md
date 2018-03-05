---
title: "New-SPVisioSafeDataProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 311e8348-6d8b-40e1-ab1d-08a002ea9b7c

description: "Adds a new data provider to a Visio Services application."
---

# New-SPVisioSafeDataProvider

Adds a new data provider to a Visio Services application.
  
```
New-SPVisioSafeDataProvider -DataProviderId <String> -DataProviderType <Int32> -VisioServiceApplication <SPVisioServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Description <String>]
```

## Detailed Description

The **New-SPVisioSafeDataProvider** cmdlet adds a new data provider to the list of safe data providers for a Visio Services application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DataProviderId** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the data provider to create. The combination of **DataProviderID** and **DataProviderType** uniquely identify a data provider for a Visio Services application. The string that identifies the data provider can be a maximum of 255 alphanumeric characters.  <br/> The type must be a valid string that identifies the data provider; for example, VisioDataProvider1.  <br/> |
|**DataProviderType** <br/> |Required  <br/> |System.Int32  <br/> |The type must be a valid identity of a data provider type.  <br/> Specifies the supported type of the data provider to add. Custom data types are supported; for example, Excel Services.  <br/> |
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> |Specifies the Visio Services application in which to add the new safe data provider.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Visio Services application (for example, MyVisioService1); or an instance of a valid **SPVisioServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Description** <br/> |Optional  <br/> |System.String  <br/> |Specifies the description of the new safe data provider.  <br/> The type must be a string with a maximum of 4096 characters.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DataProviderId** <br/> |Required  <br/> |System.String  <br/> ||
|**DataProviderType** <br/> |Required  <br/> |System.Int32  <br/> ||
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

-------------------EXAMPLE------------------------
  
```
New-SPVisioSafeDataProvider -VisioServiceApplication "VGS1" -DataProviderID "CustomProvider" -DataProviderType 5 -Description "Custom Data Provider"
```

This example creates a new safe data provider for a specified Visio Services application.
  
## See also

#### 

[Get-SPVisioSafeDataProvider](get-spvisiosafedataprovider.md)
  
[Remove-SPVisioSafeDataProvider](remove-spvisiosafedataprovider.md)
  
[Set-SPVisioSafeDataProvider](set-spvisiosafedataprovider.md)

