---
title: "Set-SPEnterpriseSearchCrawlRule"
ms.author: kpalaraj
author: kpalaraj
manager: laurawi
ms.date: 2/11/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e123808e-f140-4502-886b-031661d8c4ee

description: "Sets properties for a crawl rule."
---

# Set-SPEnterpriseSearchCrawlRule

Sets properties for a crawl rule.
  
```
Set-SPEnterpriseSearchCrawlRule -Identity <CrawlRulePipeBind> [-AccountName <String>] [-AccountPassword <SecureString>] [-AssignmentCollection <SPAssignmentCollection>] [-AuthenticationType <DefaultRuleAccess | NTLMAccountRuleAccess | BasicAccountRuleAccess | CertificateRuleAccess | FormRuleAccess | CookieRuleAccess | AnonymousAccess>] [-Confirm [<SwitchParameter>]] [-ContentClass <String>] [-CrawlAsHttp <$true | $false>] [-FollowComplexUrls <$true | $false>] [-IsAdvancedRegularExpression <$true | $false>] [-PluggableSecurityTimmerId <Int32>] [-Priority <Int32>] [-SearchApplication <SearchServiceApplicationPipeBind>] [-SuppressIndexing <$true | $false>] [-Type <InclusionRule | ExclusionRule>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE------------------
  
```
$crawlRule = Get-SPEnterpriseSearchCrawlRule -Identityfile://fileserver/root -SearchApplication mySearchServiceApp
Set-SPEnterpriseSearchCrawlRule -Identity $crawlRule -Type "ExclusionRule"
```

This example sets the type of the crawl rule pertaining to the URL,  `file://fileserver/root`, to exclude this path from future crawls.
  
## Detailed Description

A search administrator runs the **Set-SPEnterpriseSearchCrawlRule** cmdlet at initial search configuration or any other time, to set or update various attributes of a crawl rule. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlRulePipeBind  <br/> |Specifies the name of the crawl rule.  <br/> The type must be a valid crawl rule URL, such as http://server_name, or an instance of a valid **CrawlRule** object.  <br/> |
| _AccountName_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the account to be used to crawl content identified by the crawl rule.  <br/> |
| _AccountPassword_ <br/> |Optional  <br/> |System.Security.SecureString  <br/> |Specifies the password for **AccountName**.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _AuthenticationType_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.CrawlRuleAuthenticationType  <br/> |Specifies one of the following authentication types:  <br/> **BasicAccountRuleAccess** Specifies basic authentication.  <br/> **CertificateRuleAccess** Specifies the X.509 certificate name.  <br/> **NTLMAccountRuleAccess** Specifies the account name for integrated authentication.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ContentClass_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a string that is sent to the protocol handler for any content that matches the crawl rule.  <br/> |
| _CrawlAsHttp_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the crawler crawls content from a hierarchical content source as HTTP content.  <br/> |
| _FollowComplexUrls_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the index engine crawls content from URLs that contain a question mark (?).  <br/> |
| _IsAdvancedRegularExpression_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the rule has full regular expression syntax.  <br/> The default value is **False**.  <br/> |
| _PluggableSecurityTimmerId_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the ID of the custom pluggable security trimmer to use, if registered.  <br/> |
| _Priority_ <br/> |Optional  <br/> |System.Int32  <br/> |Defines where in the list of crawl rules this crawl rule is to be applied.  <br/> The priority value cannot be less than 0 or greater than or equal to the number of crawl rules for the search application.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |The name of the search application that is associated with the crawl rule to be modified.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _SuppressIndexing_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies whether the crawler excludes the content of items, to which this rule applies, from the content index.  <br/> |
| _Type_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.CrawlRuleType  <br/> |Specifies the type of crawl rule. A value of zero (0) includes the rule, and a value of 1 excludes the rule.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.CrawlRulePipeBind  <br/> ||
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
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**SuppressIndexing** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**Type** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchCrawlRule](get-spenterprisesearchcrawlrule.md)
  
[New-SPEnterpriseSearchCrawlRule](new-spenterprisesearchcrawlrule.md)
  
[Remove-SPEnterpriseSearchCrawlRule](remove-spenterprisesearchcrawlrule.md)

