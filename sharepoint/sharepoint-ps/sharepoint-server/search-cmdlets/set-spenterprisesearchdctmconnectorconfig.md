---
title: "Set-SPEnterpriseSearchDCTMConnectorConfig"
ms.author: scarletb
author: scarletb
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 639f678a-00bd-4866-a6a0-f178e2761ea8
description: "Configures the Microsoft SharePoint 2013 Indexing Connector for Documentum."
---

# Set-SPEnterpriseSearchDCTMConnectorConfig

Configures the Microsoft SharePoint 2013 Indexing Connector for Documentum.
  
```
Set-SPEnterpriseSearchDCTMConnectorConfig -ACLTranslation <Nullable> -DisplayURLPatternForContainer <String> -DisplayURLPatternForDocument <String> -Shared <SwitchParameter> [-DFSURL <String>] [-PersistDCTMACL <Nullable>] [-UnmappedAccount <Nullable>] [-UserMappingTableDBName <String>] [-UserMappingTableName <String>] [-UserMappingTableSQLInstance <String>] [-UserMappingTableSQLServer <String>]
```

## Detailed Description

Use this cmdlet to configure the Indexing Connector for Documentum.
  
> [!IMPORTANT]
> Before you run the cmdlet, you may have to perform other procedures. Which procedures you must perform depends on which connector configuration mode you choose. For more information, see [Configure and use the Documentum connector in SharePoint Server 2013](http://technet.microsoft.com/library/b17a56ea-2e7f-43c6-9a17-00ae1f5c4089.aspx). 
  
This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ACLTranslation** <br/> |Required  <br/> |System.Nullable  <br/> |Specifies how the Documentum indexing connector processes security descriptors of the documents it crawls. It is an enumeration with four possible values:  <br/> **UserMappingTable**: This is the default value. Documentum security descriptors will be translated to Windows security descriptors based on the mappings defined in a user mapping table in a database. There can be only one Documentum user mapping table per SharePoint farm, and multiple SharePoint farms can reference the same mapping table. The parameters **UserMappingTableSQLServer**, **UserMappingTableSQLInstance**, and **UserMappingTableName** must be set using the **Shared** parameter set if the **Shared** **ACLTranslation** type is **UserMappingTable** or if any repository's **ACLTranslation** type is **UserMappingTable**, even if the **Shared** **ACLTranslation** type is not **UserMappingTable**. The **UnMappedAccount** parameter is optional when **ACLTranslation** type is **UserMappingTable**.  <br/> **NoSecurity**: Documentum security descriptors are ignored at crawl time. All documents from Documentum will be searchable by any SharePoint user. This option is intended to be used with a custom security trimming solution.  <br/> **SameAccountName**: Permissions to a document are granted using the Documentum account name in the Windows domain. This setting is used when users have the same username for both Documentum and Windows domain accounts, such as a shared account in Active Directory. If a document's security descriptor contains an account name that is not an existing Windows account, that security entry is ignored.  <br/> **Claims**: The Documentum security descriptor is encoded in a claims format. This is intended to be used with the Documentum custom security trimmer included with the indexing connector.  <br/> The **ACLTranslation** parameter must be supplied when the **Shared** parameter set is used. If this setting has not been configured using the **Shared** parameter set, you must supply this parameter when you use the **Repository** parameter set. If this setting has been configured using the **Shared** parameter set, then this parameter is optional when using the **Repository** parameter set.  <br/> A repository-specific setting overrides the **Shared** setting.  <br/> |
|**DisplayURLPatternForContainer** <br/> |Required  <br/> |System.String  <br/> |This parameter sets the format of the display URL for Documentum folders and cabinets. The value of this parameter must be a valid URL. There are two placeholders that can be used in this URL:  <br/>  _{ObjectId}_ - This placeholder will be replaced with the Documentum object ID.  <br/>  _{RepositoryName}_ - This placeholder will be replaced with the Documentum repository name.  <br/> The following example is an example of a folder or cabinet which would be accessible from a Documentum Webtop server named "MyWebtopServer" on port 20000:  <br/> - **DisplayURLPatternForContainer** " http://MyWebtopServer:20000/webtop/drl/objectId/{ObjectId}"  <br/> This parameter must be supplied when the **Shared** parameter set is used. If this setting has not been configured using the **Shared** parameter set, you must supply this parameter when you use the **Repository** parameter set. If this setting has been configured using the **Shared** parameter set, then this parameter is optional when using the **Repository** parameter set.  <br/> A repository-specific setting overrides the **Shared** setting.  <br/> |
|**DisplayURLPatternForDocument** <br/> |Required  <br/> |System.String  <br/> |This parameter sets the format of the display URL for Documentum documents. The value of this parameter must be a valid URL. There are three placeholders that can be used in this URL:  <br/>  _{ObjectId}_ - This placeholder will be replaced with the Documentum object ID.  <br/>  _{RepositoryName}_ - This placeholder will be replaced with the Documentum repository name.  <br/>  _{Format}_ - This placeholder will be replaced by the MIME type of the attachment to the document. If there is no attachment, this will be replaced with an empty string.  <br/> The following example is an example of a document which would be accessible from a Documentum Webtop server named "MyWebtopServer" on port 20000:  <br/> - **DisplayURLPatternForContainer** " http://MyWebtopServer:20000/webtop/drl/objectId/{ObjectId}/format/{Format}"  <br/> This parameter must be supplied when the **Shared** parameter set is used. If this setting has not been configured using the **Shared** parameter set, you must supply this parameter when you use the **Repository** parameter set. If this setting has been configured using the **Shared** parameter set, then this parameter is optional when using the **Repository** parameter set.  <br/> A repository-specific setting overrides the **Shared** setting.  <br/> |
|**Remove** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Mandatory switch parameter for the repository removal parameter set.  <br/> |
|**Repository** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Mandatory switch parameter for the repository-specific configuration parameter set.  <br/> |
|**RepositoryName** <br/> |Required  <br/> |System.String  <br/> |Supplies the repository name. This name is case sensitive and should match the Documentum repository name.  <br/> This parameter must be supplied when using either the **Repository** or **Remove** parameter set.  <br/> |
|**Shared** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> |Mandatory switch parameter for the shared configuration parameter set.  <br/> |
|**DFSURL** <br/> |Optional  <br/> |System.String  <br/> |Specifies one or more DFS web service URLs for one or more repositories. The format of this parameter's value is a repository name followed by one or more DFS web service URLs, each separated with a single backslash. More than one repository can be specified by separating repositories by a double backslash. The following example specifies the DFS web service URLs of two repositories. Repository Alpha has one DFS web service URL and repository Beta has two:  <br/> - **DFSURL** " Alpha\http://dfsAlpha:10000/services\\Beta\http://dfsBetaOne:10000/services\http://dfsBetaTwo:10000/services"  <br/> This parameter may be used only with the **Shared** parameter set.  <br/> |
|**DFSWebServiceURL** <br/> |Optional  <br/> |System.String[]  <br/> |Specifies the DFS web service URLs for the named repository.  <br/> This parameter is part of the **Repository** parameter set. If the specified repository has no DFS web service URLs, you must supply this parameter with at least one DFS web service URL. If the specified repository has one or more DFS web service URL, this parameter is optional.  <br/> |
|**IndexAllVersions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |If this parameter is set to **True**, all versions of all documents for the named repository will be indexed instead of just the current version. You should specify this parameter only if you have a specific requirement to index all versions of a document.  <br/> This parameter may be used only with the **Repository** parameter set.  <br/> |
|**PersistDCTMACL** <br/> |Optional  <br/> |System.Nullable  <br/> |This parameter is obsolete and has no function. You should not use this parameter.  <br/> |
|**UnmappedAccount** <br/> |Optional  <br/> |System.Nullable  <br/> |This parameter is used only when the **ACLTranslation** mode is set to **UserMappingTable**. This parameter sets the behavior when a Documentum account is not found in the user mapping table. It is an enumeration with two possible values:  <br/> **DiscardACE**: This is the default value. The indexing connector for Documentum discards a Documentum account when no mapped Windows domain account is found. If there is any other mapped account for the document, the document will be crawled. If none of the Documentum accounts for a document can be mapped, the document will not be added to the search index and an error will be reported for this document in the crawl log.  <br/> **AssumeSameAccount**: If a Documentum account does not have a mapping in the user mapping table, the connector will try to map the Documentum account to an account in the Windows domain with the same username. If no such account exists, the security entry will be ignored.  <br/> This parameter may be used with both the **Shared** and **Repository** parameter sets.  <br/> A repository specific setting overrides the **Shared** setting.  <br/> |
|**UserMappingTableDBName** <br/> |Optional  <br/> |System.String  <br/> |Name of the SQL Server database which contains the user mapping table.  <br/> This parameter may be used only with the **Shared** parameter set.  <br/> |
|**UserMappingTableName** <br/> |Optional  <br/> |System.String  <br/> |Name of the user mapping table.  <br/> This parameter may be used only with the **Shared** parameter set.  <br/> |
|**UserMappingTableSQLInstance** <br/> |Optional  <br/> |System.String  <br/> |Name of the SQL Server instance that contains the user mapping table.  <br/> This parameter may be used only with the **Shared** parameter set.  <br/> |
|**UserMappingTableSQLServer** <br/> |Optional  <br/> |System.String  <br/> |Host name of the SQL Server that contains the user mapping table.  <br/> This parameter may be used only with the **Shared** parameter set.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ACLTranslation** <br/> |Required  <br/> |System.Nullable  <br/> ||
|**DisplayURLPatternForContainer** <br/> |Required  <br/> |System.String  <br/> ||
|**DisplayURLPatternForDocument** <br/> |Required  <br/> |System.String  <br/> ||
|**Remove** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Repository** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**RepositoryName** <br/> |Required  <br/> |System.String  <br/> ||
|**Shared** <br/> |Required  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DFSURL** <br/> |Optional  <br/> |System.String  <br/> ||
|**DFSWebServiceURL** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**IndexAllVersions** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PersistDCTMACL** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**UnmappedAccount** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**UserMappingTableDBName** <br/> |Optional  <br/> |System.String  <br/> ||
|**UserMappingTableName** <br/> |Optional  <br/> |System.String  <br/> ||
|**UserMappingTableSQLInstance** <br/> |Optional  <br/> |System.String  <br/> ||
|**UserMappingTableSQLServer** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

------------------EXAMPLE 1-----------------
  
```
Set-SPEnterpriseSearchDCTMConnectorConfig -Shared -ACLTranslation UserMappingTable -DisplayURLPatternForContainer "http://WebTopServer:20000/webtop/component/drl?objectId={ObjectId}&amp;RepositoryName={RepositoryName}" -DisplayURLPatternForDocument "http://WebTopServer:20000/webtop/component/drl?objectId={ObjectId}&amp;format={Format}&amp;RepositoryName={RepositoryName}" -UnmappedAccount "DiscardACE" -UserMappingTableSQLServer "YourDatabaseServerName" -UserMappingTableSQLInstance "YourDatabaseInstanceName" -UserMappingTableDBName "YourMappingDatabaseName" -UserMappingTableName "YourMappingTableName"
```

```
Set-SPEnterpriseSearchDCTMConnectorConfig -Repository -RepositoryName "RepositoryOne" -DFSWebServiceURL @("http://DFSWebServices:30000/services", "http://DFSWebServices2:30000/services")
```

```
Set-SPEnterpriseSearchDCTMConnectorConfig -Repository -RepositoryName "RepositoryTwo" -DFSWebServiceURL @("http://DFSWebServices:30000/services")
```

This example configures the Indexing Connector for Documentum to index two repositories, RepositoryOne, and RepositoryTwo. The connector is configured to use a user mapping table, and common display URL patterns are set. The repositories and their respective DFS web service URLs are then added to the configuration.
  
------------------EXAMPLE 2-----------------
  
```
Set-SPEnterpriseSearchDCTMConnectorConfig -Shared -ACLTranslation UserMappingTable -DisplayURLPatternForContainer "http://WebTopServer:20000/webtop/component/drl?objectId={ObjectId}&amp;RepositoryName={RepositoryName}" -DisplayURLPatternForDocument "http://WebTopServer:20000/webtop/component/drl?objectId={ObjectId}&amp;format={Format}&amp;RepositoryName={RepositoryName}" -UnmappedAccount "DiscardACE" -UserMappingTableSQLServer "YourDatabaseServerName" -UserMappingTableSQLInstance "YourDatabaseInstanceName" -UserMappingTableDBName "YourMappingDatabaseName" -UserMappingTableName "YourMappingTableName"
```

```
Set-SPEnterpriseSearchDCTMConnectorConfig -Repository -RepositoryName "RepositoryOne" -DFSWebServiceURL @("http://DFSWebServices:30000/services", "http://DFSWebServices2:30000/services")
```

```
Set-SPEnterpriseSearchDCTMConnectorConfig -Repository -RepositoryName "RepositoryTwo" -DFSWebServiceURL @("http://DFSWebServices:30000/services") -ACLTranslation SameAccountName
```

```
Set-SPEnterpriseSearchDCTMConnectorConfig -Repository -RepositoryName "RepositoryThree" -DFSWebServiceURL @("http://DFSWebServices2:30000/services") -ACLTranslation Claims
```

This example configures the Documentum indexing connector to index three repositories, RepositoryOne, RepositoryTwo and RepositoryThree. The connector is configured to use a user mapping table, and common display URL patterns are set. The repositories and their respective DFS web service URLs are then added to the configuration. The repositories are individually configured, with their DFS web service URLs and the **ACLTranslation** settings of RepositoryTwo and RepositoryThree are overridden. 
  
Any repositories that are subsequently added will use the user mapping table, unless that setting is overridden.
  
------------------EXAMPLE 3-----------------
  
```
Set-SPEnterpriseSearchDCTMConnectorConfig -Remove -RepositoryName "RepositoryTwo"
```

This example assumes you have run the PowerShell commands as listed in Example 2. This example removes RepositoryTwo from the configuration.
  
------------------EXAMPLE 4-----------------
  
```
Set-SPEnterpriseSearchDCTMConnectorConfig -Shared -ACLTranslation UserMappingTable -DisplayURLPatternForContainer "http://WebTopServer:20000/webtop/component/drl?objectId={ObjectId}&amp;RepositoryName={RepositoryName}" -DisplayURLPatternForDocument "http://WebTopServer:20000/webtop/component/drl?objectId={ObjectId}&amp;format={Format}&amp;RepositoryName={RepositoryName}" -UnmappedAccount "DiscardACE" -UserMappingTableSQLServer "YourDatabaseServerName" -UserMappingTableSQLInstance "YourDatabaseInstanceName" -UserMappingTableDBName "YourMappingDatabaseName" -UserMappingTableName "YourMappingTableName"Set-SPEnterpriseSearchDCTMConnectorConfig -Remove -RepositoryName "RepositoryTwo"
```

```
Set-SPEnterpriseSearchDCTMConnectorConfig -Repository -RepositoryName "RepositoryOne" -DFSWebServiceURL @("http://DFSWebServices:30000/services", "http://DFSWebServices2:30000/services") -DisplayURLPatternForContainer "http://DifferentWebTopServer:20000/webtop/component/drl?objectId={ObjectId}&amp;RepositoryName={RepositoryName}" -DisplayURLPatternForDocument "http://DifferentWebTopServer:20000/webtop/component/drl?objectId={ObjectId}&amp;format={Format}&amp;RepositoryName={RepositoryName}"
```

```
Set-SPEnterpriseSearchDCTMConnectorConfig -Repository -RepositoryName "RepositoryTwo" -DFSWebServiceURL @("http://DFSWebServices:30000/services") -ACLTranslation SameAccountName
```

```
Set-SPEnterpriseSearchDCTMConnectorConfig -Repository -RepositoryName "RepositoryThree" -DFSWebServiceURL @("http://DFSWebServices2:30000/services") -ACLTranslation NoSecurity -IndexAllVersions
```

This example specifies different display URL patterns for RepositoryOne, and it sets the **IndexAllVersions** switch parameter for RepositoryThree. 
  
------------------EXAMPLE 5-----------------
  
```
Set-SPEnterpriseSearchDCTMConnectorConfig -Shared -ACLTranslation Claims -DisplayURLPatternForContainer "http://WebTopServer:20000/webtop/component/drl?objectId={ObjectId}&amp;RepositoryName={RepositoryName}" -DisplayURLPatternForDocument "http://WebTopServer:20000/webtop/component/drl?objectId={ObjectId}&amp;format={Format}&amp;RepositoryName={RepositoryName}" -DFSURL "RepositoryOne\http://DFSWebServices:10000/services\\RepositoryTwo\http://DFSWebServices2:20000/services\http://DFSWebServices3:30000/services"
```

This example uses a single cmdlet invocation to fully configure two repositories.
  

