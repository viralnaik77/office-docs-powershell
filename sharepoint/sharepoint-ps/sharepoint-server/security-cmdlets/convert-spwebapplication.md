---
title: "Convert-SPWebApplication"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 11/30/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b583685-3a10-44c9-a0b9-36b17ae3ae11

description: "Converts the authentication mode of a web application."
---

# Convert-SPWebApplication

Converts the authentication mode of a web application.
  
```
Convert-SPWebApplication -From <String> -Identity <SPWebApplicationPipeBind> -To <String> [-Database <SPContentDatabase>] [-Force <SwitchParameter>] [-LoggingDirectory <String>] [-MapList <String>] [-RetainPermissions <SwitchParameter>] [-SiteSubsriptionId <Guid>] [-SkipPolicies <SwitchParameter>] [-SkipSites <SwitchParameter>] [-SourceSkipList <String>] [-TrustedProvider <SPTrustedIdentityTokenIssuerPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]

```

## Example

------------EXAMPLE-------
  
```
Convert-SPWebApplication -Identity "https://<webappurl>" -To Claims -RetainPermissions [-Force]
```

This example converts a web application specified by the **Identity** parameter to use the claim authentication mode. 
  
## Detailed Description

Use the **Convert-SPWebApplication** cmdlet to convert the authentication mode of a Web application to Windows Claims authentication mode and migrate the user accounts in the content database to claims encoded values. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _From_ <br/> |Required  <br/> |System.String  <br/> |Specifies the string **Legacy** as the authentication mode that you want to convert from.  <br/> |
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPWebApplicationPipeBind  <br/> |Specifies the URL of the web application that you want to convert, for example: http://mysite/app1  <br/> |
| _To_ <br/> |Required  <br/> |System.String  <br/> |Specifies the string **Claims** that dictates that the application needs to be converted to claims authentication mode.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Database_ <br/> |Optional  <br/> |Microsoft.SharePoint.Administration.SPContentDatabase  <br/> |Specifies the name of the content database to migrate.  <br/> |
| _Force_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Forces the conversion of the web application.  <br/> |
| _LoggingDirectory_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a directory where verbose logs about the results of the migration will be written.  <br/> |
| _MapList_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a file containing as list of rows in the following format: user-key, migrated-user-name ,migrated-user-key.  <br/> This lets the caller customize the migration behavior.  <br/> |
| _RetainPermissions_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies the account under which the cmdlet is run and retains the permission in the web application.  <br/> |
| _SiteSubsriptionId_ <br/> |Optional  <br/> |System.Guid  <br/> |Specifies the GUID fo the Site Subscription.  <br/> |
| _SkipPolicies_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies the **SPWebApplication** security policies will not be migrated.  <br/> |
| _SkipSites_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies the SPWebApplication's SPSites will not be migrated.  <br/> |
| _SourceSkipList_ <br/> |Optional  <br/> |System.String  <br/> |Specifies a file containing as list of rows in the following format: user-key.  <br/> This lets the caller specify accounts that should be skipped.  <br/> |
| _TrustedProvider_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPTrustedIdentityTokenIssuerPipeBind  <br/> |When you migrate from a trusted login provider this is how you specify which trusted login provider.  <br/> |
   

