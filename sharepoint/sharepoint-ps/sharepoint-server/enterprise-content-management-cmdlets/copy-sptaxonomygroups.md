---
title: "Copy-SPTaxonomyGroups"
ms.author: kirks
author: Techwriter40
ms.date: 2/22/2017
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: 0fa5b4fa-b7e8-40b4-981e-5d6b5381155e

description: "Copies SharePoint Taxonomy groups from a local on-premises term store to remote SharePoint Online term store."
---

# Copy-SPTaxonomyGroups

Copies SharePoint Taxonomy groups from a local on-premises term store to remote SharePoint Online term store.
  
```
Copy-SPTaxonomyGroups -Credential <PSCredential> -GroupNames <String[]> -LocalSiteUrl <Uri> -LocalTermStoreName <String> -RemoteSiteUrl <Uri> [-AssignmentCollection <SPAssignmentCollection>] [-AuthEndpoint <String>] [-GraphApiEndpoint <String>]

```

## Example

-------------------EXAMPLE 1-------------------
  
```
$credential = Get-Credential
```

```
Copy-SPTaxonomyGroups -LocalTermStoreName "Managed Metadata Service Application Proxy" -LocalSiteUrl "http://localhost" -RemoteSiteUrl "http://contoso.com" -GroupNames "Group1","Group2" -Credential $credential
```

This example copies two taxonomy groups "Group1" and "Group2" from local Term Store to the remote Term Store in "http://contoso.com". These two sites have been enabled with Hybrid Taxonomy.
  
## Detailed Description

Use the **Copy-SPTaxonomyGroups** cmdlet to copy specified Metadata groups from an on-premises environment to SharePoint Online in a Hybrid SharePoint setup. 
  
> [!NOTE]
> This cmdlet was first available in the November 2016 PU for SharePoint Server 2016 (Feature Pack 1). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Credential_ <br/> |Required  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the Taxonomy Term Store administrator credential of remote SharePoint Online Term Store.  <br/> > [!NOTE]> Writes data to remote Term Store, so a Term Store Administrator's credential is needed to perform the operations.           |
| _GroupNames_ <br/> |Required  <br/> |System.String[]  <br/> |Specifies the name array of Taxonomy groups in local on-premises term store that will be copied to remote SharePoint Online Term store.  <br/> > [!NOTE]> The default People, Search, Search Dictionaries, SiteCollection, and System term groups cannot be copied by using the **Copy-SPTaxonomyGroups** cmdlet. Including one of these groups in the array of the **GroupNames** parameter will cause the operation to fail and an error message will be displayed. >  If you have moved one of the default term sets (that is, Company Inclusions, Company Exclusions, Query Spelling Check Inclusions, Query Spelling Check Exclusions, Location, Department, Job Title, Community Site Navigation, Generic Site Navigation, MySite Navigation) from one of these groups into a different group, that group will not be copied.           |
| _LocalSiteUrl_ <br/> |Required  <br/> |System.Uri  <br/> |Specifies the Url of local SharePoint on-premises site that contains the local Taxonomy Term Store.  <br/> |
| _LocalTermStoreName_ <br/> |Required  <br/> |System.String  <br/> |Specifies the name of local Taxonomy Term Store in the SharePoint on-premises farm.  <br/> |
| _RemoteSiteUrl_ <br/> |Required  <br/> |System.Uri  <br/> |Specifies the Url of remote SharePoint Online site that contains remote Taxonomy Term Store.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _AuthEndpoint_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the Azure Active Directory Graph API authentication endpoint. By default, the well-known endpoint will be used.  <br/> |
| _GraphApiEndpoint_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the Azure Active Directory Graph API endpoint. By default, the well-known endpoint will be used.  <br/> |
   
## See also

#### 

[Stop-SPTaxonomyReplication](stop-sptaxonomyreplication.md)

