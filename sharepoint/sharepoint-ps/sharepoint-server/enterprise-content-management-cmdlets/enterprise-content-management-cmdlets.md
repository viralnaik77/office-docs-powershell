---
title: "Enterprise content management cmdlets in SharePoint Server 2016"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 11/7/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: c4536fbd-87dc-410f-a09b-a2111d95e240
description: "Summary: List Windows PowerShell cmdlets that help you manage content in SharePoint Server 2016 environments."
---

# Enterprise content management cmdlets in SharePoint Server 2016

 **Summary:** List Windows PowerShell cmdlets that help you manage content in SharePoint Server 2016 environments. 
  
Enterprise content management (ECM) is the strategies, methods, and tools used to obtain, retain, and deliver content and documents related to processes within an organization. In SharePoint Server 2016, Microsoft PowerShell cmdlets focus on two aspects of content deployment functionality.
  
Content deployment copies content from a source SharePoint Server 2016 site collection to a destination site collection. You can copy the entire source site collection or a subset of sites.
> [!NOTE]
> Make sure that you run the initial content deployment as a full deployment. After you complete a full deployment, you can run an incremental deployment, which deploys only changed pages and related assets. 
  
The Microsoft PowerShell cmdlets that are related to content deployment focus on two areas:
- **Content deployment path** A content deployment path defines the relationship between a source and destination site collection for content deployment. After you create a path, you can create jobs and associate them with the path to begin deploying content. 
    
    Use the Microsoft PowerShell noun, **SPContentDeploymentPath**, to retrieve, set, and create deployment paths. 
    
- **Content deployment job** A content deployment job is associated with a content deployment path. It defines the specific content to be deployed from the source to the destination, and the schedule on which the deployment should occur. 
    
    The Microsoft PowerShell noun, **SPContentDeploymentJob**, lets the administrator retrieve, set, and create deployment jobs. 
    
This article also lists cmdlets that support administration of metadata.[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
## Content deployment

|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Get-SPContentDeploymentJob](get-spcontentdeploymentjob.md)** <br/> |Returns a content deployment job or a collection of content deployment jobs.  <br/> |
|**[Get-SPContentDeploymentPath](get-spcontentdeploymentpath.md)** <br/> |Returns a content deployment path or a collection of content deployment paths.  <br/> |
|**[Get-SPSiteSubscriptionEdiscoveryHub](get-spsitesubscriptionediscoveryhub.md)** <br/> |Displays the eDiscovery hub for a site subscription.  <br/> |
|**[Get-SPSiteSubscriptionEdiscoverySearchScope](get-spsitesubscriptionediscoverysearchscope.md)** <br/> |Displays the search scope for the eDiscovery hub of the specified site collection.  <br/> |
|**[New-SPContentDeploymentJob](new-spcontentdeploymentjob.md)** <br/> |Creates a content deployment job.  <br/> |
|**[New-SPContentDeploymentPath](new-spcontentdeploymentpath.md)** <br/> |Creates a new content deployment path.  <br/> |
|**[Remove-SPContentDeploymentJob](remove-spcontentdeploymentjob.md)** <br/> |Removes a content deployment job.  <br/> |
|**[Remove-SPContentDeploymentPath](remove-spcontentdeploymentpath.md)** <br/> |Removes a content deployment path.  <br/> |
|**[Set-SPContentDeploymentJob](set-spcontentdeploymentjob.md)** <br/> |Sets properties of a content deployment job.  <br/> |
|**[Set-SPContentDeploymentPath](set-spcontentdeploymentpath.md)** <br/> |Sets properties of a content deployment path.  <br/> |
|**[Set-SPSiteSubscriptionEdiscoveryHub](set-spsitesubscriptionediscoveryhub.md)** <br/> |Sets properties for the eDiscovery hub of a site subscription.  <br/> |
|**[Start-SPContentDeploymentJob](start-spcontentdeploymentjob.md)** <br/> |Starts a content deployment job.  <br/> |
   
## Metadata administration

|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Clear-SPMetadataWebServicePartitionData](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/clear-spmetadatawebservicepartitiondata.md)** <br/> |Removes all data for a site subscription on a metadata Web service application  <br/> |
|**[Export-SPMetadataWebServicePartitionData](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/export-spmetadatawebservicepartitiondata.md)** <br/> |Exports the data from a metadata Web service for a site subscription.  <br/> |
|**[Get-SPMetadataServiceApplication](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/get-spmetadataserviceapplication.md)** <br/> |Returns the properties of a service application or a collection of service applications.  <br/> |
|**[Get-SPMetadataServiceApplicationProxy](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/get-spmetadataserviceapplicationproxy.md)** <br/> |Returns the properties of a service application proxy or a collection of service application proxies.  <br/> |
|**[Get-SPSiteSubscriptionMetadataConfig](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/get-spsitesubscriptionmetadataconfig.md)** <br/> |Returns the site subscription configuration settings for a metadata service application.  <br/> |
|**[Get-SPTaxonomySession](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/get-sptaxonomysession.md)** <br/> |Returns a TaxonomySession object.  <br/> |
|**[Import-SPMetadataWebServicePartitionData](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/import-spmetadatawebservicepartitiondata.md)** <br/> |Restores the data for a site subscription.  <br/> |
|**[New-SPMetadataServiceApplication](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/new-spmetadataserviceapplication.md)** <br/> |Creates a new metadata service application.  <br/> |
|**[New-SPMetadataServiceApplicationProxy](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/new-spmetadataserviceapplicationproxy.md)** <br/> |Creates a new metadata service application proxy.  <br/> |
|**[Remove-SPSiteSubscriptionMetadataConfig](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/remove-spsitesubscriptionmetadataconfig.md)** <br/> |Removes site subscription configuration settings.  <br/> |
|**[Set-SPMetadataServiceApplication](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/set-spmetadataserviceapplication.md)** <br/> |Sets the properties for a metadata service application.  <br/> |
|**[Set-SPMetadataServiceApplicationProxy](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/set-spmetadataserviceapplicationproxy.md)** <br/> |Sets the properties for a metadata service application proxy.  <br/> |
|**[Set-SPSiteSubscriptionMetadataConfig](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/managed-metadata-cmdlets/set-spsitesubscriptionmetadataconfig.md)** <br/> |Sets the site subscription configuration settings for a specified metadata service application.  <br/> |
   
 **Hybrid auditing**
  
|||
|:-----|:-----|
|**[Copy-SPTaxonomyGroups](copy-sptaxonomygroups.md)** <br/> |Copies SharePoint Taxonomy groups from a local on-premises term store to remote SharePoint Online term store.  <br/> |
|**[Stop-SPTaxonomyReplication](stop-sptaxonomyreplication.md)** <br/> |Terminates Hybrid SharePoint Taxonomy replication from SharePoint Online site to local SharePoint on-premises site.  <br/> |
   
## See also

#### 

[Microsoft PowerShell for SharePoint Server reference](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/microsoft-powershell-for-sharepoint-server-reference.md)

