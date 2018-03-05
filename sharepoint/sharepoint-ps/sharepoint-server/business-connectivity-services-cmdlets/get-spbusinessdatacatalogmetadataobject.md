---
title: "Get-SPBusinessDataCatalogMetadataObject"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/24/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d0b5439-7037-41dc-91a5-3aaed43d81f4

description: "Returns a Business Data Connectivity Metadata Store metadata object."
---

# Get-SPBusinessDataCatalogMetadataObject

Returns a Business Data Connectivity Metadata Store metadata object.
  
```
Get-SPBusinessDataCatalogMetadataObject -BdcObjectType <Catalog | Model | LobSystem | LobSystemInstance | Entity> -ServiceContext <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-ContainingLobSystem <String>] [-Name <String>] [-Namespace <String>]
```

## Detailed Description

The **Get-SPBusinessDataCatalogMetadataObject** cmdlet reads a Business Data Connectivity Metadata Store metadata object from a Business Data Connectivity Service application. Output for this cmdlet can be a series of objects. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**BdcObjectType** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SharedService.SPGetSPBusinessDataCatalogMetadataObjectCmdlet+PSBdcObjectType  <br/> |Specifies the type of the metadata object to return.  <br/> The type must be one of the following valid metadata object types: **BdcCatalog**, **Model**, **LobSystem**, **LobSystemInstance**, or **Entity**.  <br/> |
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context of the Business Data Connectivity Metadata Store metadata object to return.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**ContainingLobSystem** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the LobSystem.  <br/> |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the metadata object.  <br/> |
|**Namespace** <br/> |Optional  <br/> |System.String  <br/> |Specifies the namespace of the metadata object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**BdcObjectType** <br/> |Required  <br/> |Microsoft.SharePoint.BusinessData.SharedService.SPGetSPBusinessDataCatalogMetadataObjectCmdlet+PSBdcObjectType  <br/> ||
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**ContainingLobSystem** <br/> |Optional  <br/> |System.String  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**Namespace** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

------------------EXAMPLE------------------
  
```
$Model = Get-SPBusinessDataCatalogMetadataObject -BdcObjectType "Model" -Name "ContosoModel" -ServiceConext http://contoso
```

This example gets a metadata object of type  `Model` with the name  `ContosoModel` from the Business Data Connectivity Metadata Store on the given site. 
  
## See also

#### 

[Set-SPBusinessDataCatalogMetadataObject](set-spbusinessdatacatalogmetadataobject.md)
  
[Grant-SPBusinessDataCatalogMetadataObject](grant-spbusinessdatacatalogmetadataobject.md)
  
[Revoke-SPBusinessDataCatalogMetadataObject](revoke-spbusinessdatacatalogmetadataobject.md)

