---
title: "Get-SPODataConnectionSetting"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 99058d65-691e-4916-9258-5ffeff4e38ad

description: "Returns Business Connectivity Services OData connection properties."
---

# Get-SPODataConnectionSetting

Returns Business Connectivity Services OData connection properties.
  
```
Get-SPODataConnectionSetting -ServiceContext <SPServiceContextPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Name <String>]
```

## Detailed Description

Use the **Get-SPODataConnectionSetting** cmdlet to display Business Connectivity Services OData connection properties for a specified Business Connectivity Services connection. 
  
If the name of the connection is not specified by using the **Name** parameter, this cmdlet will return the list of the connections for the specified BDC service context. 
  
> [!NOTE]
> This cmdlet applies to an on-premises environment only. You cannot use this command in the SharePoint Online Management Shell. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> |Specifies the service context which is in the form of an instance of an **SPServiceContext** object, an **SPSiteAdministration** object identifier, or a **SPSite** object. An example of a service context value is an identifier from the ID field, a string identifier, a URI, or a string representation of a GUID.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Name** <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the Business Connectivity Services connection object.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ServiceContext** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceContextPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

----------------EXAMPLE 1------------ 
  
```
Get-SPODataConnectionSetting -ServiceContext  "http://contoso" -Name "ContosoServiceApp"
```

This example returns properties of the BCS connection named **ContosoServiceApp**
  
----------------EXAMPLE 2------------ 
  
```
Get-SPODataConnectionSetting -ServiceContext "http://contoso"
```

This example returns a list of BCS connections for the service context named **http://contoso**
  
## See also

#### 

[New-SPODataConnectionSetting](new-spodataconnectionsetting.md)
  
[Remove-SPODataConnectionSetting](remove-spodataconnectionsetting.md)
  
[Set-SPODataConnectionSetting](set-spodataconnectionsetting.md)

