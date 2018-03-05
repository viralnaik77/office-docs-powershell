---
title: "Set-SPEnterpriseSearchCrawlContentSource"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 216538e0-f729-4d4d-80a9-b34ab892ef44

description: "Sets the properties of a crawl content source for a Search service application."
---

# Set-SPEnterpriseSearchCrawlContentSource

Sets the properties of a crawl content source for a Search service application.
  
```
Set-SPEnterpriseSearchCrawlContentSource <COMMON PARAMETERS>

```

## Example

------------------EXAMPLE------------------
  
```
$searchapp = Get-SPEnterpriseSearchServiceApplication "SearchApp1"$cs = Get-SPEnterpriseSearchCrawlContentSource -SearchApplication $searchapp ""$cs | Set-SPEnterpriseSearchCrawlContentSource -ScheduleType Full -DailyCrawlSchedule -CrawlScheduleRunEveryInterval 30$cs | Set-SPEnterpriseSearchCrawlContentSource -ScheduleType Incremental -DailyCrawlSchedule -CrawlScheduleRepeatInterval 60 -CrawlScheduleRepeatDuration 1440
```

This example returns an existing content source  `ExampleContentSource1`, and creates a schedule to run a full crawl every 30 days and an incremental crawl every hour every day.
  
## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810). 
  
The **Set-SPEnterpriseSearchCrawlContentSource** cmdlet updates the rules of a crawl content source when the search functionality is initially configured and after any new content source is added. This cmdlet is called once to set the incremental crawl schedule for a content source, and it is called again to set a full crawl schedule. 
  
The value of the optional EnableContinuousCrawls parameter can be True or False. A value of True enables continuous crawls of items in this content source. This causes the search system to automatically start incremental crawls to process the latest changes to items in the corresponding data repositories. This helps to keep the index fresh for items in this content source. Search service application administrators can still configure full crawls as needed.
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ContentSourcePipeBind  <br/> |Specifies the crawl content source to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a **ContentSource** object (for example, ContentSource1); or an instance of a valid **ContentSource** object.  <br/> |
| _ScheduleType_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ContentSourceCrawlScheduleType  <br/> |Specifies the type of crawl schedule.  <br/> The type must be one of the following values: Full or Incremental.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _BDCApplicationProxyGroup_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> |Specifies the proxy to use for a **business** type content source. This proxy group must contain a default Business Data Connectivity Metadata Store proxy.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _CrawlPriority_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.CrawlPriority  <br/> |Specifies the priority of this content source.  <br/> The type must be one of the following integers: 1= Normal, 2=High.  <br/> |
| _CrawlScheduleDaysOfMonth_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the days on which to crawl when the **MonthlyCrawlSchedule** parameter is set.  <br/> |
| _CrawlScheduleDaysOfWeek_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.DaysOfWeek  <br/> |Specifies the days on which to crawl when the **WeeklyCrawlSchedule** parameter is set.  <br/> |
| _CrawlScheduleMonthsOfYear_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Administration.MonthsOfYear  <br/> |Specifies the months on which to crawl when the **MonthlyCrawlSchedule** parameter is set.  <br/> |
| _CrawlScheduleRepeatDuration_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of times to repeat the crawl schedule.  <br/> |
| _CrawlScheduleRepeatInterval_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of minutes between each repeat interval for the crawl schedule  <br/> |
| _CrawlScheduleRunEveryInterval_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the interval between crawls.  <br/> When the **DailyCrawlSchedule** parameter is set, specifies the number of days between crawls.  <br/> When the **WeeklyCrawlSchedule** parameter is set, specifies the number of weeks between crawls.  <br/> |
| _CrawlScheduleStartDateTime_ <br/> |Optional  <br/> |System.DateTime  <br/> |Specifies the initial date of the crawl. The default value is midnight on the current day.  <br/> |
| _CustomProtocol_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the custom protocol, handled by the custom connector, to use for this content source.  <br/> |
| _DailyCrawlSchedule_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Base schedule on days between crawls.  <br/> |
| _EnableContinuousCrawls_ <br/> |Optional  <br/> |System.Boolean  <br/> |Specifies the value of the EnableContinuousCrawls parameter: True or False.  <br/> |
| _LOBSystemSet_ <br/> |Optional  <br/> |System.String[]  <br/> |Specifies a comma-separated list of Business Data Connectivity Metadata Store system names and system instance names for a **business** type content source.  <br/> |
| _MaxPageEnumerationDepth_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies, for a **web** or **custom** type content source, the number of page hops that the crawler can make from the start address to a content item.  <br/> |
| _MaxSiteEnumerationDepth_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies, for a **web** or **custom** type content source, the number of site hops that the crawler can take from the start address to a content item.  <br/> |
| _MonthlyCrawlSchedule_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Base the schedule on months between crawls.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the new display name for the content source.  <br/> The type must be a valid name of a content source; for example, ContentSource1.  <br/> |
| _RemoveCrawlSchedule_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Deletes the specified crawl.  <br/> |
| _SearchApplication_ <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search application that contains the content source.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid **SearchServiceApplication** object.  <br/> |
| _StartAddresses_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the comma-separated list of URLs at which to start a crawl for this content source.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _Tag_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the URL for the page to modify the settings for a custom content source. The string that specifies the URL can contain a maximum of 1,024 characters.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _WeeklyCrawlSchedule_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Base the schedule on weeks between crawls.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.ContentSourcePipeBind  <br/> ||
|**ScheduleType** <br/> |Required  <br/> |System.Nullable  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**BDCApplicationProxyGroup** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyGroupPipeBind  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**CrawlPriority** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**CrawlScheduleDaysOfMonth** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**CrawlScheduleDaysOfWeek** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**CrawlScheduleMonthsOfYear** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**CrawlScheduleRepeatDuration** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**CrawlScheduleRepeatInterval** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**CrawlScheduleRunEveryInterval** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**CrawlScheduleStartDateTime** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**CustomProtocol** <br/> |Optional  <br/> |System.String  <br/> ||
|**DailyCrawlSchedule** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**EnableContinuousCrawls** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**LOBSystemSet** <br/> |Optional  <br/> |System.String[]  <br/> ||
|**MaxPageEnumerationDepth** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MaxSiteEnumerationDepth** <br/> |Optional  <br/> |System.Nullable  <br/> ||
|**MonthlyCrawlSchedule** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**RemoveCrawlSchedule** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**SearchApplication** <br/> |Optional  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**StartAddresses** <br/> |Optional  <br/> |System.String  <br/> ||
|**Tag** <br/> |Optional  <br/> |System.String  <br/> ||
|**WeeklyCrawlSchedule** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPEnterpriseSearchCrawlContentSource](get-spenterprisesearchcrawlcontentsource.md)
  
[New-SPEnterpriseSearchCrawlContentSource](new-spenterprisesearchcrawlcontentsource.md)
  
[Remove-SPEnterpriseSearchCrawlContentSource](remove-spenterprisesearchcrawlcontentsource.md)

