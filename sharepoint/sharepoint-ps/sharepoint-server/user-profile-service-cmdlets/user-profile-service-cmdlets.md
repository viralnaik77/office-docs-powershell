---
title: "Use Windows PowerShell cmdlets to configure the User Profile service in SharePoint Server 2016"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 3/1/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: 419b63a1-a0fd-4421-b184-81040ebb0b8e

description: "Summary: Learn about the Windows PowerShell cmdlets that you can use to configure the User Profile Service in SharePoint Server 2016."
---

# Use Windows PowerShell cmdlets to configure the User Profile service in SharePoint Server 2016

 **Summary:** Learn about the Windows PowerShell cmdlets that you can use to configure the User Profile Service in SharePoint Server 2016. 
  
In SharePoint Server 2016, the User Profile Service is used to store and process information about users. This information is stored as a collection of user profile properties per user. The user information must be imported into the user profile store before it can be used by various personalization-related features and people search. These properties can be imported from line-of-business applications and directory services (primarily Active Directory directory service and Lightweight Directory Access Protocol (LDAP)).
  
SharePoint Server 2016 provides an enterprise-wide repository for storing social and expertise tags and for associating those tags with a user's profile. Administrators can control who can tag items on a given site, decide which tags can be used, and delete tags prior to a specific date or based on a specific user profile ID. Tagging relies on the Managed Metadata Service and can be enabled by using either the UI or PowerShell cmdlets.
  
You can use PowerShell cmdlets for the User Profile Service to create and configure the User Profile Service and profile tags, and to configure permissions and all global settings for the User Profile Service.
  
Cmdlets that have an ![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png) icon next to them are new cmdlets in SharePoint Server 2016. 
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Get-SPMicrofeedOptions](get-spmicrofeedoptions.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Returns the feed cache settings for the current user profile application.  <br/> |
|**[Update-SPMicrofeedOptions](update-spmicrofeedoptions.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Updates the feed cache settings for the current user profile application.  <br/> |
|**[Add-SPSiteSubscriptionProfileConfig](add-spsitesubscriptionprofileconfig.md)** <br/> |Adds a new site subscription to a User Profile Service application.  <br/> |
|**[Get-SPProfileServiceApplicationSecurity](get-spprofileserviceapplicationsecurity.md)** <br/> |Returns permission and identity information.  <br/> |
|**[Move-SPProfileManagedMetadataProperty](move-spprofilemanagedmetadataproperty.md)** <br/> |Moves multiple-string values into a term set.  <br/> |
|**[New-SPProfileServiceApplication](new-spprofileserviceapplication.md)** <br/> |Adds a User Profile Service application to a farm.  <br/> |
|**[New-SPProfileServiceApplicationProxy](new-spprofileserviceapplicationproxy.md)** <br/> |Creates a User Profile Service application proxy on the local farm.  <br/> |
|**[Remove-SPActivityItems](remove-spactivityitems.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Removes activity events from the published and consolidated tables.  <br/> |
|**[Remove-SPSiteSubscriptionProfileConfig](remove-spsitesubscriptionprofileconfig.md)** <br/> |Deletes a site subscription from a User Profile Service application.  <br/> |
|**[Remove-SPSocialItemByDate](remove-spsocialitembydate.md)** <br/> |Deletes tags, notes, or ratings.  <br/> |
|**[Set-SPDefaultProfileConfig](set-spdefaultprofileconfig.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Changes the MySitesPublicEnabled property of the User Profile Application Proxy .  <br/> |
|**[Set-SPProfileServiceApplication](set-spprofileserviceapplication.md)** <br/> |Sets properties of a User Profile Service application.  <br/> |
|**[Set-SPProfileServiceApplicationProxy](set-spprofileserviceapplicationproxy.md)** <br/> |Sets properties of a proxy for a User Profile Service application.  <br/> |
|**[Set-SPProfileServiceApplicationSecurity](set-spprofileserviceapplicationsecurity.md)** <br/> |Sets permission and identity information.  <br/> |
|**[Set-SPSiteSubscriptionProfileConfig](set-spsitesubscriptionprofileconfig.md)** <br/> |Sets the parameters of a site subscription.  <br/> |
|**[Upgrade-SPProfileServiceApplication](upgrade-spprofileserviceapplication.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Upgrades User Profile Service and its related profile and social store.  <br/> |
|**[Update-SPProfilePhotoStore](update-spprofilephotostore.md)** <br/> |Updates the profile photo store to be compatible with SharePoint Server 2016.  <br/> |
|**[Add-SPPluggableSecurityTrimmer](http://technet.microsoft.com/library/ab8617f1-6622-48e4-9a12-25eb9b3833c0.aspx)** <br/> |Adds a pluggable security trimmer to a User Profile service application proxy.  <br/> |
|**[Get-SPPluggableSecurityTrimmer](http://technet.microsoft.com/library/adf108e1-e1ab-4019-a216-f91e4bbfcf2a.aspx)** <br/> |Gets pluggable security trimmers that have been added to a User Profile service application proxy.  <br/> |
|**[Remove-SPPluggableSecurityTrimmer](http://technet.microsoft.com/library/b933f351-c958-4833-9778-60171780b147.aspx)** <br/> |Removes pluggable security trimmers that have been added to a User Profile service application proxy.  <br/> |
|**[Add-SPProfileLeader](add-spprofileleader.md)** <br/> |Adds a company leader.  <br/> |
|**[Get-SPProfileLeader](get-spprofileleader.md)** <br/> |Returns the current company leaders.  <br/> |
|**[Remove-SPProfileLeader](remove-spprofileleader.md)** <br/> |Removes a company leader.  <br/> |
|**[Move-SPSocialComment](move-spsocialcomment.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Moves social comments.  <br/> |
|**[Update-SPRepopulateMicroblogFeedCache](update-sprepopulatemicroblogfeedcache.md)** <br/> |Refreshes the cache.  <br/> |
|**[Update-SPRepopulateMicroblogLMTCache](update-sprepopulatemicrobloglmtcache.md)** <br/> |Refreshes the cache.  <br/> |
|**[Export-SPTagsAndNotesData](export-sptagsandnotesdata.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Exports the SharePoint Newsfeed tags and notes.  <br/> |
   
## See also

#### 

[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md)

