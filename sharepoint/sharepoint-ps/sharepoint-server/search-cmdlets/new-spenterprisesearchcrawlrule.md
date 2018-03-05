---
title: "New-SPEnterpriseSearchCrawlRule"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f299d577-acd6-4da3-975e-f0a0b9092aa8

description: "Creates a new crawl rule."
---

# New-SPEnterpriseSearchCrawlRule

Creates a new crawl rule.
  
```
New-SPEnterpriseSearchCrawlRule -Path <String> -SearchApplication <SearchServiceApplicationPipeBind> -Type <InclusionRule | ExclusionRule> [-AccountName <String>] [-AccountPassword <SecureString>] [-AssignmentCollection <SPAssignmentCollection>] [-AuthenticationType <DefaultRuleAccess | NTLMAccountRuleAccess | BasicAccountRuleAccess | CertificateRuleAccess | FormRuleAccess | CookieRuleAccess | AnonymousAccess>] [-Confirm [<SwitchParameter>]] [-ContentClass <String>] [-CrawlAsHttp <$true | $false>] [-FollowComplexUrls <$true | $false>] [-IsAdvancedRegularExpression <$true | $false>] [-PluggableSecurityTimmerId <Int32>] [-Priority <Int32>] [-SuppressIndexing <$true | $false>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------ 
  
```
New-SPEnterpriseSearchCrawlRule -SearchApplication mySearchServiceApp -Identity http://ExampleSharePointSite -CrawlAsHttp 1 -Type InclusionRule
```

This example creates an inclusion type crawl rule for the site at  `http://ExampleSharePointSite`. The rule specifies that the site be crawled as an HTTP site.
  
## Detailed Description

The **New-SPEnterpriseSearchCrawlRule** cmdlet creates special rules for crawling items that are contained in the specified path. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Path_ <br/> |Required  <br/> |System.String  <br/> |Specifies a unique path to which a crawl rule applies.  <br/> |
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the Search application that is associated with the crawl rule to be modified.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _Type_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.CrawlRuleType  <br/> |Specifies the type of crawl rule. A value of zero (0) includes the rule, a value of 1 excludes the rule.  <br/> |
| _AccountName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the account to use when applying the crawl rule.  <br/> |
| _AccountPassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the account to use when applying the crawl rule.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _AuthenticationType_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.CrawlRuleAuthenticationType  <br/> |Specifies one of the following authentication types to access matching URLs:  <br/> **BasicAccountRuleAccess** — Specifies the account name and password that are required for this authentication type.  <br/> **CertificateRuleAccess** — Specifies the valid client certificate name that is required for this authentication type.  <br/> **NTLMAccountRuleAccess** — Specifies the account name for integrated authentication.  <br/> **FormRuleAccess** — Specifies a valid URL for HTTP POST or HTTP GET, public and private parameters, and a list of error pages that are used by this authentication type.  <br/> **CookieRuleAccess** — Specifies private parameters and a list of error pages that are used by this authentication type.  <br/> **AnonymousAccess** — Specifies that the matching URLs have to be accessed anonymously.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ContentClass_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the string that is sent to the protocol handler for any content that matches the crawl rule.  <br/> |
| _CrawlAsHttp_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the crawler should crawl content from a hierarchical content source as HTTP content.  <br/> |
| _FollowComplexUrls_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the index engine should crawl content with URLs that contain a question mark (?).  <br/> |
| _IsAdvancedRegularExpression_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the rule has a full regular expression syntax.  <br/> The default value is **False**.  <br/> |
| _PluggableSecurityTimmerId_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the ID of the custom pluggable security trimmer to use, if registered.  <br/> |
| _Priority_ <br/> |Optional  <br/> |System.Int32  <br/> |Defines where in the list of crawl rules this crawl rule should be applied.  <br/> The priority value cannot be less than 0 or greater than or equal to the number of crawl rules for the search application.  <br/> |
| _SuppressIndexing_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the crawler should exclude the content of items that this rule applies to from the content index.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Path** <br/> |Required  <br/> |System.String  <br/> ||
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**Type** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Administration.CrawlRuleType  <br/> ||
|**AccountName** <br/> |Optional  <br/> |System.String  <br/> ||
|**AccountPassword** <br/> |Optional  <br/> |System.Security.SecureString  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**AuthenticationType** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ContentClass** <br/> |Optional  <br/> |System.String  <br/> ||
|**CrawlAsHttp** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**FollowComplexUrls** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**IsAdvancedRegularExpression** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**PluggableSecurityTimmerId** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Priority** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**SuppressIndexing** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Set-SPEnterpriseSearchCrawlRule](set-spenterprisesearchcrawlrule.md)
  
[Get-SPEnterpriseSearchCrawlRule](get-spenterprisesearchcrawlrule.md)
  
[Remove-SPEnterpriseSearchCrawlRule](remove-spenterprisesearchcrawlrule.md)

