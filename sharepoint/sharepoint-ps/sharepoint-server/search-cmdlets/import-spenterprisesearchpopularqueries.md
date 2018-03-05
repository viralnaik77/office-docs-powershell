---
title: "Import-SPEnterpriseSearchPopularQueries"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 810a552b-60a3-496a-b891-c5ddf911b90f

description: "Imports queries from a comma-separated list. The search box will suggest these queries as users type."
---

# Import-SPEnterpriseSearchPopularQueries

Imports queries from a comma-separated list. The search box will suggest these queries as users type.
  
```
Import-SPEnterpriseSearchPopularQueries -ResultSource <Source> -SearchApplicationProxy <SearchServiceApplicationProxyPipeBind> -Web <SPWeb> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Filename <String>] [-WhatIf [<SwitchParameter>]]

```

## Example

--------EXAMPLE--------
  
```
$ssap = Get-SPEnterpriseSearchServiceApplicationProxy
```

```
$hostname = hostname
```

```
$web = get-spsite | get-spweb | where {$_.Url-eq "http://$hostname"}
```

```
$owner = new-object Microsoft.Office.Server.Search.Administration.SearchObjectOwner -ArgumentList @([Microsoft.Office.Server.Search.Administration.SearchObjectLevel]::SPWeb,$web)
```

```
$mgr = new-object Microsoft.Office.Server.Search.Administration.Query.FederationManager -ArgumentList $ssap
```

```
$source = $mgr.GetSourceByName("Local SharePoint Results", $owner)
```

```
Import-SPEnterpriseSearchPopularQueries -SearchApplicationProxy $ssap -Filename C:\input.txt -ResultSource $source -Web $web
```

This example uses the **Import-SPEnterpriseSearchPopularQueries** cmdlet to import the queries file that is named C:\input.txt and associate with it the Result Source referenced by **$source** and the SPWeb referenced by **$web**. The example defines the variable **$web** as the SPWeb with URL http://hostname, and the variable **$source** as the Result Source named "Local SharePoint Results" at the SPWeb referenced by **$web**. 
  
## Detailed Description

The **Import-SPEnterpriseSearchPopularQueries** cmdlet imports queries from a comma-separated list. As the user types a query in the search box, the search box will suggest queries from the comma-separated list. The search box bases these suggestions on: 
  
- The SPWeb the search box is located on.
  
- The Result Source configured on the search box.
  
For example, if the search box is located on the "Engineering" SPWeb, the suggested queries will differ from if the search box is located on the "Management" SPWeb. Likewise, if the Result Source on the search box is "Local SharePoint Results", the suggested queries will differ from if the Result Source is "Conversations".
  
The comma-separated list must consist of one line per query, where each line contains the following items: 
  
 *Query Text*  . The actual query expression. 
  
 *Query Count*  . The number of times this query was executed. 
  
 *Click Count*  . The number of times any user clicked any result for this query. 
  
 *LCID*  . The locale identifier (LCID) for the language of the query. 
  
Each line must use the formatting: Query Text,Query Count,Click Count,LCID. For example,  `Company store,100,80,1033`. For suggestions to appear in the search box, the Click Count value must be more than five. The search box ranks query suggestions by their Click Count values (approximately).
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ResultSource_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.Query.Source  <br/> |Specifies the Result Source to associate with the imported queries. The type must be an instance of a valid Source object.  <br/> |
| _SearchApplicationProxy_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> |Specifies the proxy for the search application to which the queries file should be imported. The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application proxy name (for example, SearchAppProxy1); or an instance of a valid **SearchServiceApplicationProxy** object.  <br/> |
| _Web_ <br/> |Required  <br/> |Microsoft.SharePoint.SPWeb  <br/> |Specifies the SPWeb to associate with the imported queries. The type must be an instance of a valid SPWeb object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _Filename_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the full UNC (Universal Naming Convention) path of the file to import.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ResultSource** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.Query.Source  <br/> ||
|**SearchApplicationProxy** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationProxyPipeBind  <br/> ||
|**Web** <br/> |Required  <br/> |Microsoft.SharePoint.SPWeb  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Filename** <br/> |Optional  <br/> |System.String  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

