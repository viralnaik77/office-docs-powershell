---
title: "Get-SPProfilePropertyCollection"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4471ae54-d3b0-49ef-83aa-9fa251853eb6
description: "Gets all user profile properties."
---

# Get-SPProfilePropertyCollection

Gets all user profile properties.
  
```
Get-SPProfilePropertyCollection [-Source] <String>
```

## Detailed Description

> [!IMPORTANT]
> This cmdlet has been deprecated for SharePoint Server 2016 and is not available for use. 
  
The **Get-SPProfilePropertyCollection** cmdlet returns an object that contains a collection of all profile property subtypes from the source server. You can pipe the resulting object to other User Profile Replication Engine cmdlets. 
  
> [!NOTE]
> Duplicate profile property subtypes are removed. 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Source** <br/> |Required  <br/> |System.String  <br/> |Specifies the URL of the My Site Host from where the user profiles are retrieved, for example, http://hq.contoso.com:8081/my.  <br/> |
   
## AutoGenParams

> [!IMPORTANT]
> This cmdlet has been deprecated for SharePoint Server 2016 and is not available for use. 
  
|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Source** <br/> |Required  <br/> |System.String  <br/> ||
   
## Example

----------Example ---------- 
  
```
get-spprofilepropertycollection -source http://hq.contoso.com:8081
```

> [!IMPORTANT]
> This cmdlet has been deprecated for SharePoint Server 2016 and is not available for use. 
  
This example gets all of the profile property subtypes from hq.contoso.com.
  
## See also

#### 

[Stop-SPProfileServiceIncrementalReplication](http://technet.microsoft.com/library/1ad28561-1af4-4984-b98f-d5746b564ce1.aspx)

