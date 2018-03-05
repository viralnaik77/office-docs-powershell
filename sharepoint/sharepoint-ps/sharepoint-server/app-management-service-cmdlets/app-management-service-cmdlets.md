---
title: "App Management Service cmdlets in SharePoint Server 2016"
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
ms.assetid: e00548da-4f70-46b6-8ee2-4c21fbfdd009

description: "Summary: Provides a list of Windows PowerShell cmdlets that you can use to manage apps in SharePoint Server 2016."
---

# App Management Service cmdlets in SharePoint Server 2016

 **Summary:** Provides a list of Windows PowerShell cmdlets that you can use to manage apps in SharePoint Server 2016. 
  
You can use the App Management cmdlets to add specific information or functionality to a SharePoint site.
  
Cmdlets that have an ![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png) icon next to them are new cmdlets in SharePoint Server 2016. 
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Add-SPAppDeniedEndpoint](add-spappdeniedendpoint.md)** <br/> |Adds an endpoint to the apps denied endpoint list.  <br/> |
|**[Clear-SPAppDeniedEndpoints](http://technet.microsoft.com/library/0ed45c68-dc70-4d6e-b13a-dee87620ff99.aspx)** <br/> |Obsolete. For the replacement, see [Clear-SPAppDeniedEndpointList](clear-spappdeniedendpointlist.md).  <br/> |
|**[Clear-SPAppDeniedEndpointList](clear-spappdeniedendpointlist.md)** <br/> |Removes all app-denied endpoints.  <br/> |
|**[Disable-SPAppAutoProvision](disable-spappautoprovision.md)** <br/> |Disables automatic provisioning of an app.  <br/> |
|**[Enable-SPAppAutoProvision](enable-spappautoprovision.md)** <br/> |Enables automatic provisioning of an app.  <br/> |
|**[Export-SPAppPackage](export-spapppackage.md)** <br/> |Exports an app package.  <br/> |
|**[Get-SPAppAcquisitionSettings](http://technet.microsoft.com/library/aace199a-63b3-43f4-9771-82c661f72768.aspx)** <br/> |Obsolete. For the replacement, see [Get-SPAppAcquisitionConfiguration](get-spappacquisitionconfiguration.md) <br/> |
|**[Get-SPAppAcquisitionConfiguration](get-spappacquisitionconfiguration.md)** <br/> |Returns app acquisition settings.  <br/> |
|**[Get-SPAppAutoProvisionConnection](get-spappautoprovisionconnection.md)** <br/> |Returns provision connection settings for an app.  <br/> |
|**[Get-SPAppDeniedEndpoints](http://technet.microsoft.com/library/fad7a182-1abc-4238-898d-ab56afb75c88.aspx)** <br/> |Obsolete. For the replacement, see [Get-SPAppDeniedEndpointList](get-spappdeniedendpointlist.md) <br/> |
|**[Get-SPAppDeniedEndpointList](get-spappdeniedendpointlist.md)** <br/> |Gets the App denied endpoint list.  <br/> |
|**[Get-SPAppDomain](get-spappdomain.md)** <br/> |Gets the domain used to host app.  <br/> |
|**[Get-SPAppHostingQuotas](http://technet.microsoft.com/library/9780e129-80b7-4f83-a4d6-4b1ec7103eae.aspx)** <br/> |Obsolete. For the replacement, see [Get-SPAppHostingQuotaConfiguration](get-spapphostingquotaconfiguration.md) <br/> |
|**[Get-SPAppHostingQuotaConfiguration](get-spapphostingquotaconfiguration.md)** <br/> |Returns the hosting quotas for an app.  <br/> |
|**[Get-SPAppInstance](get-spappinstance.md)** <br/> |Returns the metadata for an instance of an app.  <br/> |
|**[Get-SPAppMarketplaceSettings](get-spappmarketplacesettings.md)** <br/> |Obsolete. For the replacement, see [Get-SPAppStoreConfiguration](get-spappstoreconfiguration.md) <br/> |
|**[Get-SPAppStoreConfiguration](get-spappstoreconfiguration.md)** <br/> |Returns app SharePoint Store settings.  <br/> |
|**[Get-SPAppScaleProfile](get-spappscaleprofile.md)** <br/> |Returns settings for an app profile.  <br/> |
|**[Get-SPAppDisableSettings](http://technet.microsoft.com/library/db1f15c3-edb7-4786-91f6-7b21a2e9684d.aspx)** <br/> |Obsolete. For the replacement, see [Get-SPAppDisablingConfiguration](get-spappdisablingconfiguration.md) <br/> |
|**[Get-SPAppDisablingConfiguration](get-spappdisablingconfiguration.md)** <br/> |Returns the disable list sync state for an app.  <br/> |
|**[Get-SPAppStateUpdateInterval](get-spappstateupdateinterval.md)** <br/> |Returns the interval in hours between updates of the app state update job.  <br/> |
|**[Get-SPAppStateSyncLastRunTime](get-spappstatesynclastruntime.md)** <br/> |Returns the latest time the app state update job was invoked.  <br/> |
|**[Get-SPAppStoreWebServiceConfiguration](get-spappstorewebserviceconfiguration.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Returns properties of a SharePoint Store app.  <br/> |
|**[Get-SPInternalAppStateSyncLastRunTime](get-spinternalappstatesynclastruntime.md)** <br/> |Returns the latest time the internal app state update job was invoked.  <br/> |
|**[Get-SPInternalAppStateUpdateInterval](get-spinternalappstateupdateinterval.md)** <br/> |Returns the interval in hours between updates of the internal app state update job.  <br/> |
|**[Import-SPAppPackage](import-spapppackage.md)** <br/> |Imports an app package.  <br/> |
|**[Install-SPApp](install-spapp.md)** <br/> |Installs an instance of an app.  <br/> |
|**[New-SPAppManagementServiceApplication](new-spappmanagementserviceapplication.md)** <br/> |Creates an App Management Service application.  <br/> |
|**[New-SPAppManagementServiceApplicationProxy](new-spappmanagementserviceapplicationproxy.md)** <br/> |Creates an App Management Service application proxy.  <br/> |
|**[Remove-SPAppDeniedEndpoint](remove-spappdeniedendpoint.md)** <br/> |Removes an endpoint from the app denied endpoint list.  <br/> |
|**[Restart-SPAppInstanceJobs](http://technet.microsoft.com/library/582e2939-1a82-47fc-b1f5-f405f37196f3.aspx)** <br/> |Obsolete. For replacement, see [Restart-SPAppInstanceJob](restart-spappinstancejob.md) <br/> |
|**[Restart-SPAppInstanceJob](restart-spappinstancejob.md)** <br/> |Restarts an app instance.  <br/> |
|**[Set-SPAppAcquisitionSettings](http://technet.microsoft.com/library/ff22238e-06db-425c-9ec6-1781406c8c58.aspx)** <br/> |Obsolete. For the replacement, see [Set-SPAppAcquisitionConfiguration](set-spappacquisitionconfiguration.md) <br/> |
|**[Set-SPAppAcquisitionConfiguration](set-spappacquisitionconfiguration.md)** <br/> |Sets app acquisition settings.  <br/> |
|**[Set-SPAppAutoProvisionConnection](set-spappautoprovisionconnection.md)** <br/> |Sets provision connection settings for an app.  <br/> |
|**[Set-SPAppDomain](set-spappdomain.md)** <br/> |Sets the domain used to host app.  <br/> |
|**[Set-SPAppHostingQuotas](http://technet.microsoft.com/library/e09053f4-af37-4c98-82df-aeeb28bea86e.aspx)** <br/> |Obsolete. For the replacement, see [Set-SPAppHostingQuotaConfiguration](set-spapphostingquotaconfiguration.md) <br/> |
|**[Set-SPAppHostingQuotaConfiguration](set-spapphostingquotaconfiguration.md)** <br/> |Sets hosting quotas for an app.  <br/> |
|**[Set-SPAppManagementDeploymentId](set-spappmanagementdeploymentid.md)** <br/> |Sets the identifier of the farm or tenant used by the Office Marketplace to issue App licenses.  <br/> |
|**[Set-SPAppMarketplaceSettings](set-spappmarketplacesettings.md)** <br/> |Obsolete. For the replacement, see [Set-SPAppStoreConfiguration](set-spappstoreconfiguration.md) <br/> |
|**[Set-SPAppStoreConfiguration](set-spappstoreconfiguration.md)** <br/> |Sets SharePoint Store settings for an app.  <br/> |
|**[Set-SPAppStoreWebServiceConfiguration](set-spappstorewebserviceconfiguration.md)**![New cmdlet in 2016](../media/mod_icon_whatsNew_1_xs.png)           <br/> |Sets properties of a SharePoint Store app.  <br/> |
|**[Set-SPAppScaleProfile](set-spappscaleprofile.md)** <br/> |Sets settings for the app profile.  <br/> |
|**[Set-SPAppDisableSettings](http://technet.microsoft.com/library/0735aff7-4449-4ffc-a4bc-720f45e5ca25.aspx)** <br/> |Obsolete. For the replacement, see [Set-SPAppDisablingConfiguration](set-spappdisablingconfiguration.md) <br/> |
|**[Set-SPAppDisablingConfiguration](set-spappdisablingconfiguration.md)** <br/> |Sets the disable list sync state for an app.  <br/> |
|**[Set-SPAppStateUpdateInterval](set-spappstateupdateinterval.md)** <br/> |Sets the interval in hours between updates of the app state update job.  <br/> |
|**[Set-SPInternalAppStateUpdateInterval](set-spinternalappstateupdateinterval.md)** <br/> |Sets the interval in hours between updates of the internal app state update job.  <br/> |
|**[Uninstall-SPAppInstance](uninstall-spappinstance.md)** <br/> |Uninstalls an instance of an app.  <br/> |
|**[Update-SPAppCatalogSettings](http://technet.microsoft.com/library/54d5c522-ecbc-4b49-bf75-e6630a5b5fda.aspx)** <br/> |Obsolete. For the replacement, see [Update-SPAppCatalogConfiguration](update-spappcatalogconfiguration.md) <br/> |
|**[Update-SPAppCatalogConfiguration](update-spappcatalogconfiguration.md)** <br/> |Sets a specific site collection as the App Catalog site collection.  <br/> |
|**[Update-SPAppInstance](update-spappinstance.md)** <br/> |Updates the app instance.  <br/> |
|**[Get-SPMarketplaceConnectionSettings](http://technet.microsoft.com/library/1e3413cb-c78c-451d-aca8-f8d0257b4cfd.aspx)** <br/> |Returns SharePoint Store settings.  <br/> |
|**[New-SPMarketplaceWebServiceApplicationProxy](new-spmarketplacewebserviceapplicationproxy.md)** <br/> |Creates a service application proxy for the app identity data web service.  <br/> |
|**[Set-SPMarketplaceConnectionSettings](http://technet.microsoft.com/library/2dbd0fb6-d8ef-4537-942b-d0297ae554bb.aspx)** <br/> |Sets SharePoint Store connection settings.  <br/> |
|**[Get-SPAppDisableSettings](http://technet.microsoft.com/library/db1f15c3-edb7-4786-91f6-7b21a2e9684d.aspx)** <br/> |Obsolete. For the replacement, see [Get-SPAppDisablingConfiguration](get-spappdisablingconfiguration.md) <br/> |
|[Get-SPAppDisablingConfiguration](get-spappdisablingconfiguration.md) <br/> |Returns the disable list sync state for an app.  <br/> |
|**[Set-SPAppDisableSettings](http://technet.microsoft.com/library/0735aff7-4449-4ffc-a4bc-720f45e5ca25.aspx)** <br/> |Obsolete. For the replacement, see [Set-SPAppDisablingConfiguration](set-spappdisablingconfiguration.md) <br/> |
|**[Set-SPAppDisablingConfiguration](set-spappdisablingconfiguration.md)** <br/> |Sets the disable list sync state for an app.  <br/> |
|**[Get-SPAppSiteSubscriptionName](get-spappsitesubscriptionname.md)** <br/> |Returns the name of the specified site subscription.  <br/> |
|**[Get-SPOfficeStoreAppsDefaultActivation](get-spofficestoreappsdefaultactivation.md)** <br/> |Returns the properties of apps for Office.  <br/> |
|**[Set-SPAppSiteSubscriptionName](set-spappsitesubscriptionname.md)** <br/> |Sets or changes the name for the specified site subscription.  <br/> |
|**[Set-SPOfficeStoreAppsDefaultActivation](set-spofficestoreappsdefaultactivation.md)** <br/> |Sets the properties of apps for Office.  <br/> |
|**[Set-SetSPAppSiteDomain](set-setspappsitedomain.md)** <br/> |Creates or changes the URL of any installed app.  <br/> |
|**[Get-SPWebApplicationAppDomain](get-spwebapplicationappdomain.md)** <br/> |Returns all app domains for a specific web application.  <br/> |
|**[New-SPWebApplicationAppDomain](new-spwebapplicationappdomain.md)** <br/> |Creates or changes a AppDomain entry.  <br/> |
|**[Remove-SPWebApplicationAppDomain](remove-spwebapplicationappdomain.md)** <br/> |Deletes the AppDomain.  <br/> |
   
## See also

#### 

[Microsoft PowerShell for SharePoint Server reference](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/microsoft-powershell-for-sharepoint-server-reference.md)

