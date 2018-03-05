---
title: "New-SPEnterpriseSearchCrawlContentSource"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5eeb0b21-d8db-436a-b353-a6bf57b6f734

description: "Creates a content source for a Search service application."
---

# New-SPEnterpriseSearchCrawlContentSource

Creates a content source for a Search service application.
  
```
New-SPEnterpriseSearchCrawlContentSource -Name <String> -SearchApplication <SearchServiceApplicationPipeBind> -Type <Business | O12Business | CustomRepository | Custom | Exchange | File | LotusNotes | SharePoint | TopicPages | Web | PushedContent> [-AssignmentCollection <SPAssignmentCollection>] [-BDCApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] [-Confirm [<SwitchParameter>]] [-CrawlPriority <Normal | High>] [-CustomProtocol <String>] [-LOBSystemSet <String[]>] [-MaxPageEnumerationDepth <Int32>] [-MaxSiteEnumerationDepth <Int32>] [-SharePointCrawlBehavior <CrawlVirtualServers | CrawlSites>] [-StartAddresses <String>] [-Tag <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication "SearchApp1"New-SPEnterpriseSearchCrawlContentSource -SearchApplication $searchapp -Type file -name somename -StartAddresses file://someserver/public
```

This example creates a new content source of type  `file` to crawl a file system. 
  
## Detailed Description

The **New-SPEnterpriseSearchCrawlContentSource** cmdlet creates a new content source. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Name_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of the content source to create.  <br/> The type must be a valid name of a **ContentSource** object (for example, ContentSource1).  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the content source.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid Search service application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _Type_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.ContentSourceType  <br/> |Specifies the name of the content source type. The value **Business** is for the Business Data Connectivity metadata store. The value **Exchange** is for Microsoft Exchange public folders. The value **Custom** is for a custom content source type.  <br/> The type must be the valid name of a content source type; for example, custom.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _BDCApplicationProxyGroup_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> |Specifies the proxy to use for a **business** type content source. This proxy group must contain a default Business Data Connectivity Metadata Store proxy.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _CrawlPriority_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.CrawlPriority  <br/> |Specifies the priority of this content source.  <br/> The value must be one of the following integers: 1= Normal, 2=High.  <br/> |
| _CustomProtocol_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the custom protocol, handled by the custom connector, to use for this content source.  <br/> |
| _LOBSystemSet_ <br/> |Optional  <br/> |System.String[]  <br/> |Specifies a comma-separated list of Business Data Connectivity metadata store system names and system instance names for a **business** type content source.  <br/> |
| _MaxPageEnumerationDepth_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies, for a **web** or **custom** type content source, the number of page hops that the crawler can make from the start address to a content item.  <br/> |
| _MaxSiteEnumerationDepth_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies, for a **web** or **custom** type content source, the number of site hops that the crawler can take from the start address to a content item.  <br/> |
| _SharePointCrawlBehavior_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.SharePointCrawlBehavior  <br/> |Specifies crawl behavior for a **sharepoint** type content source. The behavior can be either:  <br/> **CrawlSites** to crawl only particular site collections.  <br/> **CrawlVirtualServers** to crawl the entire server and all site collections on the server.  <br/> |
| _StartAddresses_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the comma-separated list of URLs at which to start a crawl for this content source.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _Tag_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the URL for the page to modify the settings for a custom content source. The string that specifies the URL can contain a maximum of 1,024 characters.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Name** <br/> |Required  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**Type** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.ContentSourceType  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**BDCApplicationProxyGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**CrawlPriority** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**CustomProtocol** <br/> |Optional  <br/> |System.String  <br/> ||
|**LOBSystemSet** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**MaxPageEnumerationDepth** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaxSiteEnumerationDepth** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SharePointCrawlBehavior** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**StartAddresses** <br/> |Optional  <br/> |System.String  <br/> ||
|**Tag** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

