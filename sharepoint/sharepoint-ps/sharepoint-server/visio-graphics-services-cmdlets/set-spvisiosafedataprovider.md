---
title: "Set-SPVisioSafeDataProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff647c1-e26e-4254-aa98-0f1e4e2b529b

description: "Specifies a description of a safe data provider for a Visio Services application."
---

# Set-SPVisioSafeDataProvider

Specifies a description of a safe data provider for a Visio Services application.
  
```
Set-SPVisioSafeDataProvider -DataProviderId <String> -DataProviderType <Int32> -Description <String> -VisioServiceApplication <SPVisioServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

The **Set-SPVisioSafeDataProvider** cmdlet sets the **Description** property of a safe data provider for a Visio Services application. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DataProviderId** <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the data provider to update. The combination of **DataProviderID** and **DataProviderType** uniquely identifies a data provider for a Visio Services application. The string that identifies the data provider can be a maximum of 255 alphanumeric characters. Custom data types are supported; for example, Excel Services.  <br/> The type must be a valid string that identifies the data provider.  <br/> |
|**DataProviderType** <br/> |Required  <br/> |System.Int32  <br/> |Specifies the supported type of the data provider to get. Custom data types are supported; for example, Excel services.  <br/> The type must be a valid identity of a data provider type.  <br/> |
|**Description** <br/> |Required  <br/> |System.String  <br/> |Specifies the description of the safe data provider to set.  <br/> The type must be a string with a maximum of 4096 characters.  <br/> |
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> |Specifies the Visio Services application that contains the **SPVisioSafeDataProvider** object.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Visio Services application (for example, MyVisioService1); or an instance of a valid **SPVisioServiceApplication** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**DataProviderId** <br/> |Required  <br/> |System.String  <br/> ||
|**DataProviderType** <br/> |Required  <br/> |System.Int32  <br/> ||
|**Description** <br/> |Required  <br/> |System.String  <br/> ||
|**VisioServiceApplication** <br/> |Required  <br/> |Microsoft.Office.Visio.Server.Cmdlet.SPVisioServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
   
## Example

-------------------EXAMPLE 1----------------------
  
```
Set-SPVisioSafeDataProvider -VisioServiceApplication "VGS1" -DataProviderID "SQLOLEDB" -DataProviderType 1 -Description "SQL OLEDB Driver!"
```

This example sets the description property of a safe data provider for a specific Visio Services application.
  
-------------------EXAMPLE 2----------------------
  
```
Get-SPVisioServiceApplication -Identity "VGS1" | Set-SPVisioSafeDataProvider -DataProviderID "SQLOLEDB" -DataProviderType 1 -Description "SQL OLEDB Driver!"
```

This example sets the  `Description` property of a safe data provider for a specific Visio Services application. The result is piped from the **Set-SPVisioSafeDataProvider** cmdlet. 
  
## See also

#### 

[Remove-SPVisioSafeDataProvider](remove-spvisiosafedataprovider.md)
  
[Get-SPVisioSafeDataProvider](get-spvisiosafedataprovider.md)
  
[New-SPVisioSafeDataProvider](new-spvisiosafedataprovider.md)

