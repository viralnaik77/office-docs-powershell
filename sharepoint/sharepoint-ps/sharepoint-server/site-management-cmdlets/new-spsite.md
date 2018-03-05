---
title: "New-SPSite"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdadc86-0cda-49b7-a84a-5cfc6b4506b3

description: "Creates a new site collection at the specified URL."
---

# New-SPSite

Creates a new site collection at the specified URL.
  
```
New-SPSite -OwnerAlias <SPUserPipeBind> -Url <String> [-AdministrationSiteType <None | TenantAdministration>] [-AssignmentCollection <SPAssignmentCollection>] [-CompatibilityLevel <Int32>] [-Confirm [<SwitchParameter>]] [-ContentDatabase <SPContentDatabasePipeBind>] [-CreateFromSiteMaster <SwitchParameter>] [-Description <String>] [-HostHeaderWebApplication <SPWebApplicationPipeBind>] [-Language <UInt32>] [-Name <String>] [-OverrideCompatibilityRestriction <SwitchParameter>] [-OwnerEmail <String>] [-QuotaTemplate <SPQuotaTemplatePipeBind>] [-SecondaryEmail <String>] [-SecondaryOwnerAlias <SPUserPipeBind>] [-SiteSubscription <SPSiteSubscriptionPipeBind>] [-Template <SPWebTemplatePipeBind>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------------EXAMPLE 1-----------------------
  
```
New-SPSite http://<site name>/sites/test -OwnerAlias "DOMAIN\JDoe" -Language 1033
```

This example creates an English site collection at  `http://<site name>/sites/test` that is owned by user  `DOMAIN\Jdow`.
  
------------------EXAMPLE 2-----------------------
  
```
$w = Get-SPWebApplication http://<site name>
```

```
New-SPSite http://www.contoso.com -OwnerAlias "DOMAIN\jdow" -HostHeaderWebApplication $w -Name "Contoso" -Template "STS#0"
```

This example creates a host header site collection. Because the template is provided, the root web of this site collection will be created.
  
------------------EXAMPLE 3-----------------------
  
```
Get-SPWebTemplate | Where{ $_.Title -eq "Team Site" } | ForEach-Object{ New-SPSite http://<site name</sites/test -OwnerAlias DOMAIN\jdow -Template $_ }
```

This example creates a site collection by using the  `"Team Site"` Web template. 
  
------------------EXAMPLE 4-----------------------
  
```
New-SPSite -URL http://<site name>/sites/testsite -OwnerAlias "DOMAIN\JDow" -Language 1033 -CompatibilityLevel 14
```

This example creates an English 14 mode site collection by using the Team site template at http://\<site name\>/sites/testsite that is owned by user DOMAIN\Jdow
  
## Detailed Description

The **New-SPSite** cmdlet creates a new site collection with the URL and owner that the **Url** and **OwnerAlias** parameters. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _OwnerAlias_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> |Specifies the user login name of the site owner.  <br/> The type must be a valid user alias, in the form, Domain\username.  <br/> |
| _Url_ <br/> |Required  <br/> |System.String  <br/> |Specifies the URL that the new site collection uses. If the URL is not a host header site, the URL must start with the the web application URL.  <br/> |
| _AdministrationSiteType_ <br/> |Optional  <br/> |Microsoft.SharePoint.SPAdministrationSiteType  <br/> |Specifies the site type.  <br/> Valid values are **None** or **TentantAdministration**.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _CompatibilityLevel_ <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the version of templates to use when creating a new **SPSite** object. This value sets the initial CompatibilityLevel value for the site collection. When this parameter is not specified, the CompatibilityLevel will default to the highest possible version for the web application depending on the CompatibilityRange setting.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
| _ContentDatabase_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPContentDatabasePipeBind  <br/> |Specifies the name or GUID of the content database in which to create the new site. If no content database is specified, the site collection is selected automatically.  <br/> The type must be a valid database name in the form, SiteContent1212, or a GUID in the form, 1234-5678-9807.  <br/> |
| _CreateFromSiteMaster_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to create a new site using the Site Master.  <br/> The valid values are **True** or **False**.  <br/> |
| _Description_ <br/> |Optional  <br/> |System.String  <br/> |Describes the new site. If no value is specified, the value is left blank.  <br/> |
| _HostHeaderWebApplication_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies that if the URL provided is a host header, the **HostHeaderWebApplication** parameter must be the name, URL, GUID, or **SPWebApplication** object for the web application in which this site collection is created. If no value is specified, the value is left blank.  <br/> The type must be a valid name in one of the following forms:  <br/> -- **WebApplication-1212** <br/> -- **A URL (for example, http://server_name)** <br/> -- **A GUID (for example, 1234-5678-9876-0987)** <br/> |
| _Language_ <br/> |Optional  <br/> |System.UInt32  <br/> |Specifies the language ID for the new site collection. If no language is specified, the site collection is created with the same language that was specified when the product was installed.  <br/> This must be a valid language identifier (LCID).  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the title of the new site collection. If no name is specified, the default name is applied.  <br/> |
| _OverrideCompatibilityRestriction_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies whether to use compatibility restriction for site.  <br/> The valid values are **True** or **False**.  <br/> |
| _OwnerEmail_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the email address of site owner. If no value is specified, the value is left blank.  <br/> The type must be a email address in the form, someone@example.com.  <br/> |
| _QuotaTemplate_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPQuotaTemplatePipeBind  <br/> |Specifies the quota template for the new site. The template must exist already. If no template is specified, no quota is applied.  <br/> |
| _SecondaryEmail_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the email address of the secondary site owner. If no value is specified, the value is left blank.  <br/> The type must be a email address, in the form, someone@example.com.  <br/> |
| _SecondaryOwnerAlias_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPUserPipeBind  <br/> |Specifies the user login credentials of the secondary site owner. If no value is specified, the value is left blank.  <br/> The type must be a valid user alias, in the form, Domain\username.  <br/> |
| _SiteSubscription_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Specifies the Site Group to get site collections.  <br/> |
| _Template_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPWebTemplatePipeBind  <br/> |Specifies the Web template for the root web of the new site collection. The template must be already installed. If no template is specified, no template is provisioned.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## See also

#### 

[Get-SPSite](get-spsite.md)
  
[Set-SPSite](set-spsite.md)
  
[Backup-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/backup-spsite.md)
  
[Move-SPSite](move-spsite.md)
  
[Restore-SPSite](../../../docs-conceptual/sharepoint-server/microsoft-powershell-for-sharepoint-server-reference/backup-and-recovery-cmdlets/restore-spsite.md)

