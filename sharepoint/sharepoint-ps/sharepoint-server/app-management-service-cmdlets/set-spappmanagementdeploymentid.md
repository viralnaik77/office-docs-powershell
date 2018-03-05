---
title: "Set-SPAppManagementDeploymentId"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0128940d-c1ad-4536-9b49-fd2229797ecc

description: "Sets the identifier of the farm or tenant used by the Office Marketplace to issue App licenses."
---

# Set-SPAppManagementDeploymentId

Sets the identifier of the farm or tenant used by the Office Marketplace to issue App licenses.
  
```
Set-SPAppManagementDeploymentId -AppManagementServiceApplication <AppManagementServiceApplication> -DeploymentId <Guid> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Identity <SPSiteSubscriptionPipeBind>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Set-SPAppManagementDeploymentId** cmdlet to set the identifier of the farm or tenant used by the Office Marketplace to issue App Licenses. To ensure you do not lose rights to the use of all Apps you have purchased on the Marketplace, do not change the deployment id unless directed by Microsoft documentation or support. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppManagementServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.AppManagement.AppManagementServiceApplication  <br/> |Specifies the app management service application object that is running on the farm.  <br/> |
|**DeploymentId** <br/> |Required  <br/> |System.Guid  <br/> |Specifies the deployment identifier value for the tenant. This parameter works in conjunction with the value that is defined with **Identity** parameter. If **Identity** parameter is omitted, then it is assumed that this deployment identifier value belongs to the farm.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> |Identifies the site subscription object representing the tenant to which the **DeploymentId** parameter is to be assigned. If the **Identity** parameter is omitted, it is assumed that the deployment identifier belongs to the farm.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppManagementServiceApplication** <br/> |Required  <br/> |Microsoft.SharePoint.AppManagement.AppManagementServiceApplication  <br/> ||
|**DeploymentId** <br/> |Required  <br/> |System.Guid  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Identity** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPSiteSubscriptionPipeBind  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------EXAMPLE 1----------
  
```
$appManagementServiceApplication = Get-SPServiceApplication | where {$_.TypeName -eq "App Management Service Application"}
```

```
Set-SPAppManagementDeploymentId -DeploymentId 3102B7C3-1866-48EE-91CB-84E20AD24BF2 -AppManagementServiceApplication $appManagementServiceApplication
```

This example sets the deployment identifier of the current farm to **3102B7C3-1866-48EE-91CB-84E20AD24BF2**.
  
-----------EXAMPLE 2----------
  
```
$appManagementServiceApplication = Get-SPServiceApplication | where {$_.TypeName -eq "App Management Service Application"}
```

```
Get-SPSiteSubscription | where{$_.Id.Id -eq "88f16a50-0530-4f3f-b749-24ef0b30d685"} | Set-SPAppManagementDeploymentId -DeploymentId 3102B7C3-1866-48EE-91CB-84E20AD24BF2 -AppManagementServiceApplication $appManagementServiceApplication
```

This example sets the deployment identifier of the tenant with the site subscription identifier **88f16a50-0530-4f3f-b749-24ef0b30d685** to **3102B7C3-1866-48EE-91CB-84E20AD24BF2**.
  

