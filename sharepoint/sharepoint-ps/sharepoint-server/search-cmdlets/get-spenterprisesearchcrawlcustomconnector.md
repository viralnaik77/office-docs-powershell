---
title: "Get-SPEnterpriseSearchCrawlCustomConnector"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd3948e9-e1b5-453e-bd2d-85be7c859339

description: "Returns a CustomConnector object type."
---

# Get-SPEnterpriseSearchCrawlCustomConnector

Returns a **CustomConnector** object type. 
  
```
Get-SPEnterpriseSearchCrawlCustomConnector -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Protocol <String>]

```

## Example

--------------------EXAMPLE----------------------
  
```
$searchApp = Get-SPEnterpriseSearchServiceApplication MySearchServiceApp$crawlConn = Get-SPEnterpriseSearchCrawlCustomConnector -SearchApplication$searchApp -Protocol "http://"
```

This example obtains a reference to all custom crawl connectors for the  `http://` protocol for a search service application named  `MySearchServiceApp`.
  
## Detailed Description

The **Identity** parameter displays a custom connector for a specified Web application. If no parameters are specified, all the objects of the **CustomConnector** object type are returned. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the Search application with which the **CustomConnector** objects are associated.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Protocol_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the string version of the protocol for which to return the **CustomConnector** object. For example, "dctm://"  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Protocol** <br/> |Optional  <br/> |System.String  <br/> ||
   
## See also

#### 

[New-SPEnterpriseSearchCrawlCustomConnector](new-spenterprisesearchcrawlcustomconnector.md)
  
[Remove-SPEnterpriseSearchCrawlCustomConnector](remove-spenterprisesearchcrawlcustomconnector.md)
  
[Get-SPEnterpriseSearchServiceApplication](get-spenterprisesearchserviceapplication.md)

