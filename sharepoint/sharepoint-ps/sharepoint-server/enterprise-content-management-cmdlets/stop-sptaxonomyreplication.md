---
title: "Stop-SPTaxonomyReplication"
ms.author: kirks
author: Techwriter40
ms.date: 11/7/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: d72bcdb3-a538-4a3f-9fcb-90fae99be40f

description: "Terminates Hybrid SharePoint Taxonomy replication from SharePoint Online site to local SharePoint on-premises site."
---

# Stop-SPTaxonomyReplication

Terminates Hybrid SharePoint Taxonomy replication from SharePoint Online site to local SharePoint on-premises site.
  
```
Stop-SPTaxonomyReplication -Credential <PSCredential> [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

-------------------EXAMPLE -------------------
  
```
$credential = Get-Credential
```

```
Stop-SPTaxonomyReplication -Credential $credential 
```

This example performs a full replication and deletes the Taxonomy Groups Replication timer job. If the full replication fails, you can run the cmdlet again.
  
## Detailed Description

Use the **Stop-SPTaxonomyReplication** cmdlet to terminate Hybrid SharePoint Taxonomy replication from SharePoint Online site to local SharePoint on-premises site. The Taxonomy Groups Replication timer job will be killed and a full replication from SharePoint Online Taxonomy store to local SharePoint on-premises store will be performed. 
  
> [!NOTE]
> This cmdlet was first available in the November 2016 PU for SharePoint Server 2016 (Feature Pack 1). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Credential_ <br/> |Required  <br/> |System.Management.Automation.PSCredential  <br/> |This is the Taxonomy Term Store administrator credential of remote SharePoint OnlineTerm Store.  <br/> > [!NOTE]> Fetches full taxonomy data properties, so a Term Store Administrator's credential is needed to perform the operations.           |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## See also

#### 

[Copy-SPTaxonomyGroups](copy-sptaxonomygroups.md)

