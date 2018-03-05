---
title: "Use Windows PowerShell cmdlets to administer and configure search in SharePoint Server 2016"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 3/2/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: de5221a4-2fd0-4684-a4db-f3735f708ee0
description: "Summary: Learn about the Windows PowerShell cmdlets that you can use to administrate and configure Search for SharePoint Server 2016."
---

# Use Windows PowerShell cmdlets to administer and configure search in SharePoint Server 2016

 **Summary:** Learn about the Windows PowerShell cmdlets that you can use to administrate and configure Search for SharePoint Server 2016. 
  
Search is composed of several components, all of which provide specific functionality that is required for Search to operate. The following tables show the Microsoft PowerShell cmdlets that you can use to configure these Search components and manage Search operations for a SharePoint farm.
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
**Administration**

|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Get-SPEnterpriseSearchStatus](get-spenterprisesearchstatus.md)** <br/> |Retrieves diagnostics information for the search components.  <br/> |
|**[New-SPEnterpriseSearchAdminComponent](new-spenterprisesearchadmincomponent.md)** <br/> |Creates a new admin component for the given topology and search service instance.  <br/> |
   
**Crawling**

|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Get-SPEnterpriseSearchCrawlContentSource](get-spenterprisesearchcrawlcontentsource.md)** <br/> |Returns a crawl content source.  <br/> |
|**[Get-SPEnterpriseSearchCrawlCustomConnector](get-spenterprisesearchcrawlcustomconnector.md)** <br/> |Returns a **CustomConnector** object type.  <br/> |
|**[Get-SPEnterpriseSearchCrawlDatabase](get-spenterprisesearchcrawldatabase.md)** <br/> |Returns a crawl store.  <br/> |
|**[Get-SPEnterpriseSearchCrawlExtension](get-spenterprisesearchcrawlextension.md)** <br/> |Returns the file types to be included in the content index.  <br/> |
|**[Get-SPEnterpriseSearchCrawlMapping](get-spenterprisesearchcrawlmapping.md)** <br/> |Returns a crawl mapping for the search application.  <br/> |
|**[Get-SPEnterpriseSearchCrawlRule](get-spenterprisesearchcrawlrule.md)** <br/> |Accesses crawl rules.  <br/> |
|**[New-SPEnterpriseSearchCrawlComponent](new-spenterprisesearchcrawlcomponent.md)** <br/> |Adds a query component to a query topology.  <br/> |
|**[New-SPEnterpriseSearchCrawlContentSource](new-spenterprisesearchcrawlcontentsource.md)** <br/> |Creates a new crawl content source for a shared search application.  <br/> |
|**[New-SPEnterpriseSearchCrawlCustomConnector](new-spenterprisesearchcrawlcustomconnector.md)** <br/> |Registers a protocol for custom crawling.  <br/> |
|**[New-SPEnterpriseSearchCrawlDatabase](new-spenterprisesearchcrawldatabase.md)** <br/> |Creates a crawl database which can be added to a search service application.  <br/> |
|**[New-SPEnterpriseSearchCrawlExtension](new-spenterprisesearchcrawlextension.md)** <br/> |Adds an extension rule to a shared search application.  <br/> |
|**[New-SPEnterpriseSearchCrawlMapping](new-spenterprisesearchcrawlmapping.md)** <br/> |Creates a crawl mapping rule for a shared search application.  <br/> |
|**[New-SPEnterpriseSearchCrawlRule](new-spenterprisesearchcrawlrule.md)** <br/> |Creates a new crawl rule.  <br/> |
|**[Remove-SPEnterpriseSearchCrawlContentSource](remove-spenterprisesearchcrawlcontentsource.md)** <br/> |Deletes a specified crawl content source from a search application.  <br/> |
|**[Remove-SPEnterpriseSearchCrawlCustomConnector](remove-spenterprisesearchcrawlcustomconnector.md)** <br/> |Removes a **CustomConnector** object.  <br/> |
|**[Remove-SPEnterpriseSearchCrawlDatabase](remove-spenterprisesearchcrawldatabase.md)** <br/> |Sets properties of a crawl database for a search service application.  <br/> |
|**[Remove-SPEnterpriseSearchCrawlExtension](remove-spenterprisesearchcrawlextension.md)** <br/> |Removes a file name extension from the list of files that can be crawled.  <br/> |
|**[Remove-SPEnterpriseSearchCrawlMapping](remove-spenterprisesearchcrawlmapping.md)** <br/> |Deletes a crawl mapping.  <br/> |
|**[Remove-SPEnterpriseSearchCrawlRule](remove-spenterprisesearchcrawlrule.md)** <br/> |Deletes a crawl rule.  <br/> |
|**[Set-SPEnterpriseSearchCrawlContentSource](set-spenterprisesearchcrawlcontentsource.md)** <br/> |Sets the properties of a crawl content source for a shared search application.  <br/> |
|**[Set-SPEnterpriseSearchCrawlDatabase](set-spenterprisesearchcrawldatabase.md)** <br/> |Sets properties of a crawl database for a search service application.  <br/> |
|**[Set-SPEnterpriseSearchCrawlRule](set-spenterprisesearchcrawlrule.md)** <br/> |Sets properties for a crawl rule.  <br/> |
|**[Set-SPEnterpriseSearchCrawlLogReadPermission](set-spenterprisesearchcrawllogreadpermission.md)** <br/> |Grants users permission to view the crawl log information.  <br/> |
|**[Get-SPEnterpriseSearchCrawlLogReadPermission](get-spenterprisesearchcrawllogreadpermission.md)** <br/> |Retrieves the list of users which have permission to access the crawl log information.  <br/> |
|**[Remove-SPEnterpriseSearchCrawlLogReadPermission](remove-spenterprisesearchcrawllogreadpermission.md)** <br/> |Removes permission to view crawl log information.  <br/> |
|**[Set-SPEnterpriseSearchDCTMConnectorConfig](set-spenterprisesearchdctmconnectorconfig.md)** <br/> |Configures the Microsoft SharePoint 2013 Indexing Connector for Documentum.  <br/> |
   
## 

**Service Application**

|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Get-SPEnterpriseSearchService](get-spenterprisesearchservice.md)** <br/> |Returns the search service for a farm.  <br/> |
|**[Get-SPEnterpriseSearchServiceApplication](get-spenterprisesearchserviceapplication.md)** <br/> |Returns the search service application for a farm.  <br/> |
|**[Get-SPEnterpriseSearchServiceApplicationProxy](get-spenterprisesearchserviceapplicationproxy.md)** <br/> |Returns the search service application proxy.  <br/> |
|**[Get-SPEnterpriseSearchServiceInstance](get-spenterprisesearchserviceinstance.md)** <br/> |Returns the search service instance for a farm.  <br/> |
|**[New-SPEnterpriseSearchServiceApplication](new-spenterprisesearchserviceapplication.md)** <br/> |Adds a search service application to a farm.  <br/> |
|**[New-SPEnterpriseSearchServiceApplicationProxy](new-spenterprisesearchserviceapplicationproxy.md)** <br/> |Adds a new search application proxy to a farm..  <br/> |
|**[Remove-SPEnterpriseSearchServiceApplication](remove-spenterprisesearchserviceapplication.md)** <br/> |Deletes a search service application.  <br/> |
|**[Remove-SPEnterpriseSearchServiceApplicationProxy](remove-spenterprisesearchserviceapplicationproxy.md)** <br/> |Deletes a search service application proxy.  <br/> |
|**[Restore-SPEnterpriseSearchServiceApplication](restore-spenterprisesearchserviceapplication.md)** <br/> |Restores a third-party backup of a search application.  <br/> |
|**[Resume-SPEnterpriseSearchServiceApplication](resume-spenterprisesearchserviceapplication.md)** <br/> |Resumes a search service application that was suspended.  <br/> |
|**[Set-SPEnterpriseSearchService](set-spenterprisesearchservice.md)** <br/> |Sets the properties of a search service for a farm.  <br/> |
|**[Set-SPEnterpriseSearchServiceApplication](set-spenterprisesearchserviceapplication.md)** <br/> |Sets the properties of a search service application for a farm.  <br/> |
|**[Set-SPEnterpriseSearchServiceApplicationProxy](set-spenterprisesearchserviceapplicationproxy.md)** <br/> |Sets properties of a search service application proxy.  <br/> |
|||
|**[Start-SPEnterpriseSearchServiceInstance](start-spenterprisesearchserviceinstance.md)** <br/> |Starts an instance of a search service.  <br/> |
|**[Stop-SPEnterpriseSearchServiceInstance](stop-spenterprisesearchserviceinstance.md)** <br/> |Stops an instance of a search manager service.  <br/> |
|**[Suspend-SPEnterpriseSearchServiceApplication](suspend-spenterprisesearchserviceapplication.md)** <br/> |Suspends a search service application, pausing all crawls and search operations, to perform a task such as system maintenance.  <br/> |
|**[Upgrade-SPEnterpriseSearchServiceApplication](upgrade-spenterprisesearchserviceapplication.md)** <br/> |Upgrades a search service application.  <br/> |
|**[Backup-SPEnterpriseSearchServiceApplicationIndex](backup-spenterprisesearchserviceapplicationindex.md)** <br/> |Takes a backup of the search index to a specified backup location.  <br/> |
|**[Restore-SPEnterpriseSearchServiceApplicationIndex](restore-spenterprisesearchserviceapplicationindex.md)** <br/> |Restores the search index from the specified backup files.  <br/> |
|**[Get-SPEnterpriseSearchOwner](get-spenterprisesearchowner.md)** <br/> |Returns the search object owner.  <br/> |
|||
   
**Querying**

|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Get-SPEnterpriseSearchQueryAndSiteSettingsService](get-spenterprisesearchqueryandsitesettingsservice.md)** <br/> |Returns the search manager service.  <br/> |
|**[Get-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance](get-spenterprisesearchqueryandsitesettingsserviceinstance.md)** <br/> |Returns the service manager service instance.  <br/> |
|**[Get-SPEnterpriseSearchQueryAndSiteSettingsServiceProxy](get-spenterprisesearchqueryandsitesettingsserviceproxy.md)** <br/> |Returns the search manager service proxy.  <br/> |
|**[Get-SPEnterpriseSearchQueryAuthority](get-spenterprisesearchqueryauthority.md)** <br/> |Returns an authoritative page.  <br/> |
|**[Get-SPEnterpriseSearchQueryDemoted](get-spenterprisesearchquerydemoted.md)** <br/> |Returns a demoted site rule.  <br/> |
|**[Get-SPEnterpriseSearchQueryKeyword](get-spenterprisesearchquerykeyword.md)** <br/> |Returns a keyword term.  <br/> |
|**[Get-SPEnterpriseSearchQuerySuggestionCandidates](get-spenterprisesearchquerysuggestioncandidates.md)** <br/> |Returns a list of queries.  <br/> |
|**[Get-SPEnterpriseSearchRankingModel](get-spenterprisesearchrankingmodel.md)** <br/> |Returns a ranking model.  <br/> |
|**[Get-SPEnterpriseSearchSecurityTrimmer](get-spenterprisesearchsecuritytrimmer.md)** <br/> |Returns a custom security trimmer.  <br/> |
|**[New-SPEnterpriseSearchQueryAuthority](new-spenterprisesearchqueryauthority.md)** <br/> |Adds an authoritative page to a shared search application.  <br/> |
|**[New-SPEnterpriseSearchQueryDemoted](new-spenterprisesearchquerydemoted.md)** <br/> |Adds a demoted site rule to a shared search application.  <br/> |
|**[New-SPEnterpriseSearchQueryKeyword](new-spenterprisesearchquerykeyword.md)** <br/> |Adds a keyword term to a shared search application.  <br/> |
|**[New-SPEnterpriseSearchRankingModel](new-spenterprisesearchrankingmodel.md)** <br/> |Adds a ranking model to a shared search application.  <br/> |
|**[New-SPEnterpriseSearchSecurityTrimmer](new-spenterprisesearchsecuritytrimmer.md)** <br/> |Adds a custom security trimmer to a shared search application.  <br/> |
|**[Remove-SPEnterpriseSearchQueryAuthority](remove-spenterprisesearchqueryauthority.md)** <br/> |Deletes an authoritative page.  <br/> |
|**[Remove-SPEnterpriseSearchQueryDemoted](remove-spenterprisesearchquerydemoted.md)** <br/> |Deletes a demoted site rule.  <br/> |
|**[Remove-SPEnterpriseSearchQueryKeyword](remove-spenterprisesearchquerykeyword.md)** <br/> |Deletes a query keyword.  <br/> |
|**[Remove-SPEnterpriseSearchRankingModel](remove-spenterprisesearchrankingmodel.md)** <br/> |Deletes a ranking model.  <br/> |
|**[Remove-SPEnterpriseSearchSecurityTrimmer](remove-spenterprisesearchsecuritytrimmer.md)** <br/> |Deletes a custom security trimmer.  <br/> |
|**[Set-SPEnterpriseSearchQueryAuthority](set-spenterprisesearchqueryauthority.md)** <br/> |Sets the properties of an authoritative page for a shared search application.  <br/> |
|**[Set-SPEnterpriseSearchRankingModel](set-spenterprisesearchrankingmodel.md)** <br/> |Sets the properties of a ranking model for a shared search application.  <br/> |
|**[Start-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance](start-spenterprisesearchqueryandsitesettingsserviceinstance.md)** <br/> |Starts an instance of a search manager service.  <br/> |
|**[Stop-SPEnterpriseSearchQueryAndSiteSettingsServiceInstance](stop-spenterprisesearchqueryandsitesettingsserviceinstance.md)** <br/> |Stops an instance of a search manager service.  <br/> |
|**[Import-SPEnterpriseSearchPopularQueries](import-spenterprisesearchpopularqueries.md)** <br/> |Sets properties of a result item type.  <br/> |
|**[Set-SPEnterpriseSearchResultItemType](set-spenterprisesearchresultitemtype.md)** <br/> |Sets properties of a result item type.  <br/> |
|**[Set-SPEnterpriseSearchQuerySpellingCorrection](set-spenterprisesearchqueryspellingcorrection.md)** <br/> |Sets the operation status of the Query Spelling Corrections (QSC) component.  <br/> |
|**[Remove-SPEnterpriseSearchResultItemType](remove-spenterprisesearchresultitemtype.md)** <br/> |Creates a new result item type.  <br/> |
|**[New-SPEnterpriseSearchResultItemType](new-spenterprisesearchresultitemtype.md)** <br/> |Creates a new Result Type.  <br/> |
|**[Import-SPEnterpriseSearchThesaurus](import-spenterprisesearchthesaurus.md)** <br/> |Deploys the dictionary to the thesaurus component in the query processing flow.  <br/> |
|**[Get-SPEnterpriseSearchResultItemType](get-spenterprisesearchresultitemtype.md)** <br/> |Returns result item types.  <br/> |
|**[Get-SPEnterpriseSearchQuerySpellingCorrection](get-spenterprisesearchqueryspellingcorrection.md)** <br/> |Returns the object that exposes the Query Spelling Correction (QSC) configuration.  <br/> |
|**[Get-SPEnterpriseSearchResultSource](get-spenterprisesearchresultsource.md)** <br/> |Retrieves a result source.  <br/> |
|**[New-SPEnterpriseSearchResultSource](new-spenterprisesearchresultsource.md)** <br/> |Creates a new result source.  <br/> |
|**[Remove-SPEnterpriseSearchResultSource](remove-spenterprisesearchresultsource.md)** <br/> |Deletes a result source.  <br/> |
|**[Set-SPEnterpriseSearchResultSource](set-spenterprisesearchresultsource.md)** <br/> |Sets properties of a result source.  <br/> |
   
**Metadata**

|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Get-SPEnterpriseSearchMetadataCategory](get-spenterprisesearchmetadatacategory.md)** <br/> |Returns a crawled property category.  <br/> |
|**[Get-SPEnterpriseSearchMetadataCrawledProperty](get-spenterprisesearchmetadatacrawledproperty.md)** <br/> |Returns a crawled property.  <br/> |
|**[Get-SPEnterpriseSearchMetadataManagedProperty](get-spenterprisesearchmetadatamanagedproperty.md)** <br/> |Returns a managed property.  <br/> |
|**[Get-SPEnterpriseSearchMetadataMapping](get-spenterprisesearchmetadatamapping.md)** <br/> |Returns the current state of a managed property mapping.  <br/> |
|**[New-SPEnterpriseSearchMetadataCategory](new-spenterprisesearchmetadatacategory.md)** <br/> |Adds a crawled property category to a search service application.  <br/> |
|**[New-SPEnterpriseSearchMetadataCrawledProperty](new-spenterprisesearchmetadatacrawledproperty.md)** <br/> |Adds a crawled property to a search application crawled property category.  <br/> |
|**[New-SPEnterpriseSearchMetadataManagedProperty](new-spenterprisesearchmetadatamanagedproperty.md)** <br/> |Adds a managed property to a shared search application.  <br/> |
|**[New-SPEnterpriseSearchMetadataMapping](new-spenterprisesearchmetadatamapping.md)** <br/> |Adds a managed property mapping to a shared search application.  <br/> |
|**[Remove-SPEnterpriseSearchMetadataCategory](remove-spenterprisesearchmetadatacategory.md)** <br/> |Deletes a crawled property category.  <br/> |
|**[Remove-SPEnterpriseSearchMetadataManagedProperty](remove-spenterprisesearchmetadatamanagedproperty.md)** <br/> |Deletes a metadata managed property.  <br/> |
|**[Remove-SPEnterpriseSearchMetadataMapping](remove-spenterprisesearchmetadatamapping.md)** <br/> |Deletes a metadata mapping from a managed property.  <br/> |
|**[Set-SPEnterpriseSearchMetadataCategory](set-spenterprisesearchmetadatacategory.md)** <br/> |Sets properties of a crawled property category for a shared search application.  <br/> |
|**[Set-SPEnterpriseSearchMetadataCrawledProperty](set-spenterprisesearchmetadatacrawledproperty.md)** <br/> |Sets the properties of a metadata crawled property for a shared search application.  <br/> |
|**[Set-SPEnterpriseSearchMetadataManagedProperty](set-spenterprisesearchmetadatamanagedproperty.md)** <br/> |Sets the properties of a metadata managed property.  <br/> |
|**[Set-SPEnterpriseSearchMetadataMapping](set-spenterprisesearchmetadatamapping.md)** <br/> |Sets the properties of a managed property mapping for a shared search application.  <br/> |
|**[Get-SPEnterpriseSearchPropertyRuleCollection](get-spenterprisesearchpropertyrulecollection.md)** <br/> |Returns the collection of rules that are applied to search results.  <br/> |
|**[Get-SPEnterpriseSearchPropertyRule](get-spenterprisesearchpropertyrule.md)** <br/> |Returns a property rule.  <br/> |
   
**Topology**

|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Import-SPEnterpriseSearchTopology](import-spenterprisesearchtopology.md)** <br/> |Imports and activates a topology from an XML file.  <br/> |
|**[Export-SPEnterpriseSearchTopology](export-spenterprisesearchtopology.md)** <br/> |Exports an existing search topology.  <br/> |
|**[Set-SPEnterpriseSearchTopology](set-spenterprisesearchtopology.md)** <br/> |Activates a given search topology.  <br/> |
|**[Remove-SPEnterpriseSearchTopology](remove-spenterprisesearchtopology.md)** <br/> |Removes an inactive search topology from a search service application.  <br/> |
|**[Remove-SPEnterpriseSearchComponent](remove-spenterprisesearchcomponent.md)** <br/> |Removes the specified search component from the given search topology.  <br/> |
|**[New-SPEnterpriseSearchTopology](new-spenterprisesearchtopology.md)** <br/> |Creates a new search topology in the given search service application.  <br/> |
|**[New-SPEnterpriseSearchQueryProcessingComponent](new-spenterprisesearchqueryprocessingcomponent.md)** <br/> |Creates a new query processing component for the given topology and search service instance.  <br/> |
|**[New-SPEnterpriseSearchIndexComponent](new-spenterprisesearchindexcomponent.md)** <br/> |Creates a new index component for the given topology and search service instance.  <br/> |
|**[New-SPEnterpriseSearchContentProcessingComponent](new-spenterprisesearchcontentprocessingcomponent.md)** <br/> |Creates a new content processing component for the given topology and search service instance.  <br/> |
|**[Get-SPEnterpriseSearchTopology](get-spenterprisesearchtopology.md)** <br/> |Retrieves one or all search topologies that belong to a given search service application.  <br/> |
   
**General**

|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Get-SPEnterpriseSearchLanguageResourcePhrase](get-spenterprisesearchlanguageresourcephrase.md)** <br/> |Returns a language resource phrase.  <br/> |
|**[Get-SPEnterpriseSearchSiteHitRule](get-spenterprisesearchsitehitrule.md)** <br/> |Returns the shared site hit rule.  <br/> |
|**[New-SPEnterpriseSearchLanguageResourcePhrase](new-spenterprisesearchlanguageresourcephrase.md)** <br/> |Adds a language resource phrase to a shared search application.  <br/> |
|**[New-SPEnterpriseSearchSiteHitRule](new-spenterprisesearchsitehitrule.md)** <br/> |Adds a new site hit rule for a search application.  <br/> |
|**[Remove-SPEnterpriseSearchLanguageResourcePhrase](remove-spenterprisesearchlanguageresourcephrase.md)** <br/> |Deletes a language resource phrase from a shared search application.  <br/> |
|**[Remove-SPEnterpriseSearchSiteHitRule](remove-spenterprisesearchsitehitrule.md)** <br/> |Deletes a site hit rule.  <br/> |
|**[Get-SPEnterpriseSearchVssDataPath](get-spenterprisesearchvssdatapath.md)** <br/> |Retrieves the index paths for all active search index components on the current server.  <br/> |
|**[Get-SPEnterpriseSearchContentEnrichmentConfiguration](get-spenterprisesearchcontentenrichmentconfiguration.md)** <br/> |Returns the content enrichment configuration for the specified search service application.  <br/> |
|**[Set-SPEnterpriseSearchPrimaryHostController](set-spenterprisesearchprimaryhostcontroller.md)** <br/> |Sets the primary search host controller for the farm.  <br/> |
|**[Set-SPEnterpriseSearchLinguisticComponentsStatus](set-spenterprisesearchlinguisticcomponentsstatus.md)** <br/> |Sets the operation status of the linguistic query and document processing components.  <br/> |
|**[Set-SPEnterpriseSearchContentEnrichmentConfiguration](set-spenterprisesearchcontentenrichmentconfiguration.md)** <br/> |Stores the specified content enrichment configuration to the search service application.  <br/> |
|**[Remove-SPEnterpriseSearchContentEnrichmentConfiguration](remove-spenterprisesearchcontentenrichmentconfiguration.md)** <br/> |Removes the current content enrichment configuration from the search service application.  <br/> |
|**[New-SPEnterpriseSearchContentEnrichmentConfiguration](new-spenterprisesearchcontentenrichmentconfiguration.md)** <br/> |Creates a new ContentEnrichmentConfiguration object.  <br/> |
|**[Get-SPEnterpriseSearchLinguisticComponentsStatus](get-spenterprisesearchlinguisticcomponentsstatus.md)** <br/> |Returns the status of the linguistic query and document processing components.  <br/> |
|**[Get-SPEnterpriseSearchHostController](get-spenterprisesearchhostcontroller.md)** <br/> |Lists the specified or all search host controllers in the farm.  <br/> |
|**[Set-SPEnterpriseSearchLinksDatabase](set-spenterprisesearchlinksdatabase.md)** <br/> |Sets properties of a links database for a search service application.  <br/> |
|**[Repartition-SPEnterpriseSearchLinksDatabases](repartition-spenterprisesearchlinksdatabases.md)** <br/> |Obsolete. For replacement, see [Move-SPEnterpriseSearchLinksDatabases](move-spenterprisesearchlinksdatabases.md) <br/> |
|**[Move-SPEnterpriseSearchLinksDatabases](move-spenterprisesearchlinksdatabases.md)** <br/> |Repartitions data across links databases.  <br/> |
|**[Remove-SPEnterpriseSearchTenantSchema](remove-spenterprisesearchtenantschema.md)** <br/> |Removes a defined search schema.  <br/> |
|**[Remove-SPEnterpriseSearchTenantConfiguration](remove-spenterprisesearchtenantconfiguration.md)** <br/> |Removes all tenant specific search settings.  <br/> |
|**[Remove-SPEnterpriseSearchLinksDatabase](remove-spenterprisesearchlinksdatabase.md)** <br/> |Deletes a links database.  <br/> |
|**[Remove-SPEnterpriseSearchFileFormat](remove-spenterprisesearchfileformat.md)** <br/> |Remove a previously registered file format from the system.  <br/> |
|**[New-SPEnterpriseSearchLinksDatabase](new-spenterprisesearchlinksdatabase.md)** <br/> |Creates a new links database for a search service application.  <br/> |
|**[New-SPEnterpriseSearchFileFormat](new-spenterprisesearchfileformat.md)** <br/> |Adds a new file format in the parsing system.  <br/> |
|**[New-SPEnterpriseSearchAnalyticsProcessingComponent](new-spenterprisesearchanalyticsprocessingcomponent.md)** <br/> |Creates a new analytics processing component for the given topology and search service instance.  <br/> |
|**[Import-SPEnterpriseSearchCustomExtractionDictionary](import-spenterprisesearchcustomextractiondictionary.md)** <br/> |Imports a custom extraction dictionary.  <br/> |
|**[Get-SPEnterpriseSearchLinksDatabase](get-spenterprisesearchlinksdatabase.md)** <br/> |Retrieves a reference to a links database.  <br/> |
|**[Get-SPEnterpriseSearchFileFormat](get-spenterprisesearchfileformat.md)** <br/> |Retrieves all parseable file formats.  <br/> |
|**[Set-SPEnterpriseSearchFileFormatState](set-spenterprisesearchfileformatstate.md)** <br/> |Enables or disables parsing of a given file format.  <br/> |
|**[Get-SPEnterpriseSearchComponent](get-spenterprisesearchcomponent.md)** <br/> |Retrieves one or all search components in a given search topology.  <br/> |
|**[Get-SPEnterpriseSearchServiceApplicationBackupStore](get-spenterprisesearchserviceapplicationbackupstore.md)** <br/> |Retrieves information about the search service application backup files.  <br/> |
   
## See also

#### 

[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md)

