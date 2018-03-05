---
title: "Copy-SPActivitiesToWorkflowService"
ms.author: kenwith
author: kenwith
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba424d50-2251-4f6b-8ba8-6fbe49acee02

description: "Copies workflow activities."
---

# Copy-SPActivitiesToWorkflowService

Copies workflow activities.
  
```
Copy-SPActivitiesToWorkflowService [-ActivityName <String>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Credential <ICredentials>] [-Force <$true | $false>] [-WhatIf [<SwitchParameter>]] [-WorkflowServiceAddress <String>]
```

## Detailed Description

Use the **Copy-SPActivitiesToWorkflowService** cmdlet to copy workflow activities installed on the SharePoint host to an instance of the Workflow Service. 
  
For additional information about workflow activities and how to obtain the list of workflow activity names, see [Workflow actions in SharePoint Designer](https://go.microsoft.com/fwlink/p/?LinkId=258199)
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ActivityName** <br/> |Optional  <br/> |System.String  <br/> |Limits the copy to a specific activity. For example, LookupSPList.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**Credential** <br/> |Optional  <br/> |System.Net.ICredentials  <br/> |Specifies the service account used to communicate with the Workflow Service.  <br/> |
|**Force** <br/> |Optional  <br/> |System.Boolean  <br/> |Copy all activities regardless of existing versions.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WorkflowServiceAddress** <br/> |Optional  <br/> |System.String  <br/> |Specifies a string of the full URI for the Workflow Service.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**ActivityName** <br/> |Optional  <br/> |System.String  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Credential** <br/> |Optional  <br/> |System.Net.ICredentials  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Boolean  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WorkflowServiceAddress** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

---------------EXAMPLE------------
  
```
$cred=[System.Net.CredentialCache]::DefaultNetworkCredentials
```

```
Copy-SPActivitiesToWorkflowService -WorkflowServiceAddress 'https://workflowhost/' -Credential $cred -Force $true
```

This example copies workflow activities to the workflowhost address using the default credentials. 
  
## See also

#### 

[Get-SPWorkflowServiceApplicationProxy](get-spworkflowserviceapplicationproxy.md)
  
[New-SPWorkflowServiceApplicationProxy](new-spworkflowserviceapplicationproxy.md)
  
[Register-SPWorkflowService](register-spworkflowservice.md)

