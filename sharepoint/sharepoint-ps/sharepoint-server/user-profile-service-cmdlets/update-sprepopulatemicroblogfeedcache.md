---
title: "Update-SPRepopulateMicroblogFeedCache"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cae292cb-7e0c-4693-8801-7ab37557dfe7

description: "Refreshes the cache."
---

# Update-SPRepopulateMicroblogFeedCache

Refreshes the cache.
  
```
Update-SPRepopulateMicroblogFeedCache -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind> [-AccountName <String>] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-SiteUrl <String>] <COMMON PARAMETERS>

```

## Example

------------EXAMPLE 1------------
  
```
Update-SPRepopulateMicroblogFeedCache -ProfileServiceApplicationProxy a4f93369-0795-4aee-8a21-46f5ade29606 -AccountName contoso\<user>
```

This example refreshes the feeds for a specific user by using the **AccountName** parameter. 
  
------------EXAMPLE 2------------
  
```
Update-SPRepopulateMicroblogFeedCache -ProfileServiceApplicationProxy a4f93369-0795-4aee-8a21-46f5ade29606 -AccountName contoso\<user> -SiteSubscription 0C37852B-34D0-418e-91C6-2AC25AF4BE5B
```

This example refreshes the feeds for a specific user by using the **AccountName** parameter. 
  
------------EXAMPLE 3------------
  
```
Update-SPRepopulateMicroblogFeedCache -ProfileServiceApplicationProxy a4f93369-0795-4aee-8a21-46f5ade29606 -SiteUrl http://test/sites/usertest -SiteSubscription 0C37852B-34D0-418e-91C6-2AC25AF4BE5B
```

This example repopulates the site entity.
  
## Detailed Description

Use the **Update-SPRepopulateMicroblogFeedCache** cmdlet to refresh the feeds of a given user. It can be used in scenarios where the automatic refresh has failed or when reverting to an old version of a user's personal site. 
  
> [!NOTE]
> When you refresh the cache, the **Update-SPRepopulateMicroblogLMTCache** cmdlet should be run first, and then the **Update-SPRepopulateMicroblogFeedCache** cmdlet second. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _ListId_ <br/> |Required  <br/> |System.Guid  <br/> |PARAMVALUE: Guid  <br/> |
| _ListRootFolderUrl_ <br/> |Required  <br/> |System.String  <br/> |PARAMVALUE: String  <br/> |
| _ProfileServiceApplicationProxy_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> | Specifies the User Profile Service application proxy to update.  <br/>  The type must be in one of the following forms:  <br/>  A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh  <br/>  A valid name of a service application proxy (for example, UserProfileSvcProxy1)  <br/>  An instance of a valid **SPServiceApplicationProxy** object  <br/> |
| _SiteId_ <br/> |Required  <br/> |System.Guid  <br/> |PARAMVALUE: Guid  <br/> |
| _WebId_ <br/> |Required  <br/> |System.Guid  <br/> |PARAMVALUE: Guid  <br/> |
| _AccountName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the user's account name for the User Profile Service application. If you don't specify this parameter, you must specify the **SiteUrl** parameter. If neither parameter is specified, an error message is displayed.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _SiteSubscription_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the account under which this service should run. This parameter is mandatory in a hosted-environment and optional in a non-hosted environment.  <br/> |
| _SiteUrl_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the Site's URL to repopulate the site feeds. If you don't specify this parameter, you must specify the **AccountName** parameter. If neither parameter is specified, an error message is displayed.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AccountName** <br/> |Required  <br/> |System.String  <br/> ||
|**ProfileServiceApplicationProxy** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**SiteSubscription** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
   
## See also

#### 

[Update-SPRepopulateMicroblogLMTCache](update-sprepopulatemicrobloglmtcache.md)

