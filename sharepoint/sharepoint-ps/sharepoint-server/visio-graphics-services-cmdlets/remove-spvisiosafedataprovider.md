---
title: "Remove-SPVisioSafeDataProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a4fce127-8475-4d91-b530-0a22e754cff6

description: "Removes a data provider from a Visio Services application."
---

# Remove-SPVisioSafeDataProvider

Removes a data provider from a Visio Services application.
  
```
Remove-SPVisioSafeDataProvider -DataProviderId <String> -DataProviderType <Int32> -VisioServiceApplication <SPVisioServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Remove-SPVisioSafeDataProvider** cmdlet deletes the safe data provider that is specified in the **DataProviderID** parameter. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DataProviderId** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the data provider to delete. The combination of **DataProviderID** and **DataProviderType** uniquely identifies a data provider for a Visio Services application. The string that identifies the data provider can be a maximum of 255 alphanumeric characters.  <br/> The type must be a valid string that identifies the data provider.  <br/> |
|**DataProviderType** <br/> |Required  <br/> |System.Int32  <br/> |Specifies the supported type of the data provider to delete.  <br/> The type must be a valid identity of a data provider type.  <br/> |
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> |Specifies the Visio Services application that contains the **SPVisioSafeDataProvider** object.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Visio Services application (for example, MyVisioService1); or an instance of a valid **SPVisioServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DataProviderId** <br/> |Required  <br/> |System.String  <br/> ||
|**DataProviderType** <br/> |Required  <br/> |System.Int32  <br/> ||
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-------------------EXAMPLE------------------------
  
```
Remove-SPVisioSafeDataProvider -VisioServiceApplication "VGS1" -DataProviderID "CustomProvider" -DataProviderType 5
```

This example removes a safe data provider for a specified Visio Services application.
  
## See also

#### 

[Get-SPVisioSafeDataProvider](get-spvisiosafedataprovider.md)
  
[New-SPVisioSafeDataProvider](new-spvisiosafedataprovider.md)
  
[Set-SPVisioSafeDataProvider](set-spvisiosafedataprovider.md)

