---
title: "Use Windows PowerShell cmdlets to manage sites in SharePoint Server 2016"
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
ms.assetid: 0a0396b2-c196-4175-8e4c-083438fd3ce2

description: "Summary: Learn about the Windows PowerShell cmdlets that you can use to manage sites in a SharePoint Server 2016 farm."
---

# Use Windows PowerShell cmdlets to manage sites in SharePoint Server 2016

 **Summary:** Learn about the Windows PowerShell cmdlets that you can use to manage sites in a SharePoint Server 2016 farm. 
  
The following table shows the Microsoft PowerShell cmdlets that you can use to manage sites in a SharePoint farm.
  
Cmdlets that have an ![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png) icon next to them are new cmdlets in SharePoint Server 2016. 
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|||
|**[Get-SPSiteMaster](get-spsitemaster.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Returns site master information.  <br/> |
|**[New-SPSiteMaster](new-spsitemaster.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Creates a site master.  <br/> |
|**[Remove-SPSiteMaster](remove-spsitemaster.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Removes a site master.  <br/> |
|**[Disable-SPWebTemplateForSiteMaster](disable-spwebtemplateforsitemaster.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Disables the site master in the farm.  <br/> |
|**[Enable-SPWebTemplateForSiteMaster](enable-spwebtemplateforsitemaster.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Creates a template for a site master.  <br/> |
|**[Get-SPWebTemplatesEnabledForSiteMaster](get-spwebtemplatesenabledforsitemaster.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Returns a list of site master web templates.  <br/> |
|**[Reset-SPSites](reset-spsites.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Synchronizes the content database with the configuration database of the farm.  <br/> |
|**[Get-SPCustomLayoutsPage](get-spcustomlayoutspage.md)** <br/> |Returns a mapping to a custom layout page.  <br/> |
|**[Get-SPUser](get-spuser.md)** <br/> |Returns the user account or accounts that match a given search criteria.  <br/> |
|**[Get-SPWeb](get-spweb.md)** <br/> |Returns all subsites that match the given criteria.  <br/> |
|**[Get-SPWebApplication](get-spwebapplication.md)** <br/> |Returns all Web applications that match the given criteria.  <br/> |
|**[Get-SPFarm](get-spfarm.md)** <br/> |Returns the local SharePoint farm.  <br/> |
|**[Get-SPProduct](get-spproduct.md)** <br/> |Returns a list of the SharePoint-related products installed in the farm and the versions of all updates installed for each product.  <br/> |
|**[Get-SPServer](get-spserver.md)** <br/> |Returns the server or servers in the farm that match the given identity.  <br/> |
|**[Get-SPDeletedSite](get-spdeletedsite.md)** <br/> |Gets a list of deleted site collections.  <br/> |
|**[Get-SPSite](get-spsite.md)** <br/> |Returns all site collections that match the given criteria.  <br/> |
|**[Get-SPSiteAdministration](get-spsiteadministration.md)** <br/> |Returns a site administration object that farm administrators can use to view certain information about site collections to which they might not have access.  <br/> |
|**[Get-SPSiteSubscription](get-spsitesubscription.md)** <br/> |Returns the site subscription for the given URL or all site subscriptions in the local farm.  <br/> |
|**[Get-SPSiteSubscriptionConfig](get-spsitesubscriptionconfig.md)** <br/> |Returns the configuration properties of a site subscription.  <br/> |
|**[Move-SPSite](move-spsite.md)** <br/> |Moves site collections from one content database to another.  <br/> |
|**[Move-SPUser](move-spuser.md)** <br/> |Migrates a user account in SharePoint 2013.  <br/> |
|**[New-SPSite](new-spsite.md)** <br/> |Creates a new site collection at the specified URL.  <br/> |
|**[New-SPSiteSubscription](new-spsitesubscription.md)** <br/> |Creates a new site subscription.  <br/> |
|**[New-SPUser](new-spuser.md)** <br/> |Adds an existing user to a SharePoint site with the designated permissions.  <br/> |
|**[New-SPWeb](new-spweb.md)** <br/> |Creates a new site in an existing site collection.  <br/> |
|**[New-SPWebApplication](new-spwebapplication.md)** <br/> |Creates a new Web application within the local farm.  <br/> |
|**[New-SPWebApplicationExtension](new-spwebapplicationextension.md)** <br/> |Creates a new zone instance for the Web application.  <br/> |
|**[Remove-SPDeletedSite](remove-spdeletedsite.md)** <br/> |Removes a deleted site collection. .  <br/> |
|**[Remove-SPSite](remove-spsite.md)** <br/> |Completely deletes an existing site collection and all subsites.  <br/> |
|**[Remove-SPSiteSubscription](remove-spsitesubscription.md)** <br/> |Removes data stored in a subscription settings service application for a set of site subscriptions.  <br/> |
|**[Remove-SPSiteSubscriptionSettings](remove-spsitesubscriptionsettings.md)** <br/> |Removes the settings service data for a specified site subscription, or finds and removes orphaned data.  <br/> |
|**[Remove-SPUser](remove-spuser.md)** <br/> |Removes a user from a Web site.  <br/> |
|**[Remove-SPWeb](remove-spweb.md)** <br/> |Completely deletes the specified Web.  <br/> |
|**[Remove-SPWebApplication](remove-spwebapplication.md)** <br/> |Deletes the specified Web application.  <br/> |
|**[Rename-SPServer](rename-spserver.md)** <br/> |Renames a server that is currently connected to the farm.  <br/> |
|**[Restore-SPDeletedSite](restore-spdeletedsite.md)** <br/> |Restores a deleted site collection.  <br/> |
|**[Set-SPServer](set-spserver.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Changes the role of the server.  <br/> |
|**[Set-SPSite](set-spsite.md)** <br/> |Configures the specified site collection.  <br/> |
|**[Set-SPSiteAdministration](set-spsiteadministration.md)** <br/> |Allows farm administrators to configure any site collection.  <br/> |
|**[Set-SPSiteSubscriptionConfig](set-spsitesubscriptionconfig.md)** <br/> |Sets the configuration properties of a site subscription.  <br/> |
|**[Set-SPSubscriptionSettingsServiceApplication](set-spsubscriptionsettingsserviceapplication.md)** <br/> |Sets properties of a subscription settings service application.  <br/> |
|**[Set-SPUser](set-spuser.md)** <br/> |Configures properties on an existing user.  <br/> |
|**[Set-SPWebApplication](set-spwebapplication.md)** <br/> |Configures the specified Web application.  <br/> |
|**[Set-SPWeb](set-spweb.md)** <br/> |Configures the specified subsite.  <br/> |
|**[Export-SPSiteSubscriptionSettings](export-spsitesubscriptionsettings.md)** <br/> |Creates a backup file of site subscription data.  <br/> |
|**[Import-SPSiteSubscriptionSettings](import-spsitesubscriptionsettings.md)** <br/> |Restores a backup of subscription site settings to the given subscription identifier.  <br/> |
|**[Get-SPDeletedSite](get-spdeletedsite.md)** <br/> |Gets a list of deleted site collections.  <br/> |
|**[Remove-SPDeletedSite](remove-spdeletedsite.md)** <br/> |Removes a deleted site collection.  <br/> |
|**[Restore-SPDeletedSite](restore-spdeletedsite.md)** <br/> |Restores a deleted site collection.  <br/> |
|**[Get-SPSiteUrl](get-spsiteurl.md)** <br/> |Displays all URL mappings for the site.  <br/> |
|**[Remove-SPSiteUrl](remove-spsiteurl.md)** <br/> |Removes an URL mapping from the site.  <br/> |
|**[Set-SPSiteUrl](set-spsiteurl.md)** <br/> |Adds or changes an URL mapping for the site.  <br/> |
|**[Get-SPSiteSubscriptionIRMConfig](get-spsitesubscriptionirmconfig.md)** <br/> |Gets the Information Rights Management (IRM) settings.  <br/> |
|**[Move-SPDeletedSite](move-spdeletedsite.md)** <br/> |Moves deleted site collections from one content database to another.  <br/> |
|**[Set-SPIRMSettings](set-spirmsettings.md)** <br/> |Sets the Information Rights Management (IRM) settings.  <br/> |
|**[Set-SPSiteSubscriptionIRMConfig](set-spsitesubscriptionirmconfig.md)** <br/> |Sets the Information Rights Management (IRM) settings.  <br/> |
|**[Get-SPIRMSettings](get-spirmsettings.md)** <br/> |Returns the Information Rights Management (IRM) settings.  <br/> |
   
## See also

#### 

[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md)

