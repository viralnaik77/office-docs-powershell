---
title: "Set-SPContentDeploymentPath"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 10/6/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e68331f6-1f2c-4559-a7ea-24ea033f8244

description: "Sets properties of a content deployment path."
---

# Set-SPContentDeploymentPath

Sets properties of a content deployment path.
  
```
Set-SPContentDeploymentPath -Identity <SPContentDeploymentPathPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Authentication <Basic | Windows>] [-CompressionEnabled <SwitchParameter>] [-Confirm [<SwitchParameter>]] [-DeploySecurityInformation <None | WssOnly | All>] [-DeployUserNamesEnabled <SwitchParameter>] [-Description <String>] [-DestinationCentralAdministrationURL <Uri>] [-EventReceiversEnabled <SwitchParameter>] [-KeepTemporaryFilesOptions <Never | Always | Failure>] [-Name <String>] [-PathAccount <PSCredential>] [-PathEnabled <SwitchParameter>] [-WhatIf [<SwitchParameter>]]

```

## Example

------------EXAMPLE-------------
  
```
Get-SPContentDeploymentPath "Path 1" | Set-SPContentDeploymentPath -PathEnabled:$false
```

This example sets the deployment path  `Path 1` to be disabled. 
  
## Detailed Description

The **Set-SPContentDeploymentPath** cmdlet sets the properties of a content deployment path for a content deployment job. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Identity_ <br/> |Required  <br/> |Microsoft.SharePoint.Publishing.Cmdlet.SPContentDeploymentPathPipeBind  <br/> |Specifies the content deployment path to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a content deployment job (for example; DeployPath1); or an instance of a valid **SPContentDeploymentPath** object.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Authentication_ <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.PathAuthenticationOption  <br/> |Sets the Windows-based authentication type that the source front-end Web server uses to communicate with the destination Web application.  <br/> The type must be one of the following values: **WindowsAuth** or **BasicAuth**.  <br/> |
| _CompressionEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Turns on compression during the export.  <br/> |
| _Confirm_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |PARAMVALUE: SwitchParameter  <br/> |
| _DeploySecurityInformation_ <br/> |Optional  <br/> |Microsoft.SharePoint.Deployment.SPIncludeSecurity  <br/> |Specifies the user and group information to include during the export operation for this content deployment path. The default value is **All**.  <br/> The type must be one of the following values: **None**, **All**, or **WssOnly** - Applies only SharePoint Foundation 2013 security settings. Includes user memberships and role assignments such as default roles, for example, Web Designer or any custom roles that extend from the default roles. The access control list (ACL) for each object is migrated. No user information defined in the DAP or LDAP servers is included.  <br/> |
| _DeployUserNamesEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specify to enable event receivers during import.  <br/> |
| _Description_ <br/> |Optional  <br/> |System.String  <br/> |Sets the description for the content deployment path. The description can contain a maximum of 4096 alphanumeric characters.  <br/> The type must be a valid string.  <br/> |
| _DestinationCentralAdministrationURL_ <br/> |Optional  <br/> |System.Uri  <br/> |Specifies the SharePoint Central Administration URL for the destination farm.  <br/> The type must be a valid URL, in the form http://server_name.  <br/> |
| _EventReceiversEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Turns on event receivers during import.  <br/> |
| _KeepTemporaryFilesOptions_ <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.TemporaryFilesOption  <br/> |Specifies that temporary files are kept after content deployment is finished.  <br/> The type must be one of the following values: **Never**, **Always**, or **OnFailure**.  <br/> |
| _Name_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the content deployment path.  <br/> The type must be a valid name of a content deployment path; for example, DeploymentPath1.  <br/> |
| _PathAccount_ <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> |Specifies the user ID that is an administrator on the Central Administration page on the destination farm.  <br/> The type must be a valid SharePoint user.  <br/> |
| _PathEnabled_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Enables the content deployment path.  <br/> |
| _WhatIf_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.Publishing.Cmdlet.SPContentDeploymentPathPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Authentication** <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.PathAuthenticationOption  <br/> ||
|**CompressionEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DeploySecurityInformation** <br/> |Optional  <br/> |Microsoft.SharePoint.Deployment.SPIncludeSecurity  <br/> ||
|**DeployUserNamesEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Description** <br/> |Optional  <br/> |System.String  <br/> ||
|**DestinationCentralAdministrationURL** <br/> |Optional  <br/> |System.Uri  <br/> ||
|**EventReceiversEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**KeepTemporaryFilesOptions** <br/> |Optional  <br/> |Microsoft.SharePoint.Publishing.Administration.TemporaryFilesOption  <br/> ||
|**Name** <br/> |Optional  <br/> |System.String  <br/> ||
|**PathAccount** <br/> |Optional  <br/> |System.Management.Automation.PSCredential  <br/> ||
|**PathEnabled** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## See also

#### 

[Get-SPContentDeploymentPath](get-spcontentdeploymentpath.md)
  
[New-SPContentDeploymentPath](new-spcontentdeploymentpath.md)
  
[Remove-SPContentDeploymentPath](remove-spcontentdeploymentpath.md)

