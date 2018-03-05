---
title: "Register-SPWorkflowService"
ms.author: kenwith
author: kenwith
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa089fb9-b0c1-444b-a26d-7e916a2b2b91

description: "Configures the SharePoint host to use a workflow service."
---

# Register-SPWorkflowService

Configures the SharePoint host to use a workflow service.
  
```
Register-SPWorkflowService -SPSite <SPSitePipeBind> -WorkflowHostUri <String> [-AllowOAuthHttp <SwitchParameter>] [-AssignmentCollection <SPAssignmentCollection>] [-Force <SwitchParameter>] [-PartitionMode <SwitchParameter>] [-ScopeName <String>]
```

## Detailed Description

Use the **Register-SPWorkflowService** cmdlet to configure the SharePoint host to use a workflow service by using the **SPSite** and **WorkflowHostUri** parameters. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
> [!TIP]
>  For more information about **WorkflowHostUri** see the following: > [Video series: Install and configure Workflow in SharePoint Server 2013](https://technet.microsoft.com/en-us/library/dn201724)> [Configure workflow in SharePoint Server 2013](https://technet.microsoft.com/en-us/library/jj658586)> [Workflow in SharePoint 2013](https://technet.microsoft.com/en-US/sharepoint/jj556245.aspx)
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SPSite** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> |Specifies a site collection to configure.  <br/> |
|**WorkflowHostUri** <br/> |Required  <br/> |System.String  <br/> |Specifies a string of the full URI for the Workflow Service.  <br/> |
|**AllowOAuthHttp** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Support OAuth over HTTP.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Use this parameter to overwrite existing configuration settings and ignore errors.  <br/> |
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Determines whether a workflow connects the farm to a single instance of the Workflow Service or connects each site subscription to its own instance of the Workflow Service.  <br/> |
|**ScopeName** <br/> |Optional  <br/> |System.String  <br/> |A name that identifies SharePoint to the workflow service.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SPSite** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPSitePipeBind  <br/> ||
|**WorkflowHostUri** <br/> |Required  <br/> |System.String  <br/> ||
|**AllowOAuthHttp** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Force** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**PartitionMode** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**ScopeName** <br/> |Optional  <br/> |System.String  <br/> ||
   
## Example

----------------EXAMPLE 1------------
  
```
Register-SPWorkflowService -SPSite 'https://myhost/mysite' -WorkflowHostUri 'http://workflowhost:12291'
```

This example configures the SharePoint host by using the **WorkflowHostUri** parameter. 
  
----------------EXAMPLE 2------------
  
```
Register-SPWorkflowService -SPSite 'https://myhost/mysite' -WorkflowHostUri 'http://workflowhost:12291' -AllowOAuthHttp -Force
```

This example configures the SharePoint host to use OAuth by using the **WorkflowHostUri** and **AllowOAuthHttp** parameters. 
  
## See also

#### 

[Get-SPWorkflowServiceApplicationProxy](get-spworkflowserviceapplicationproxy.md)
  
[New-SPWorkflowServiceApplicationProxy](new-spworkflowserviceapplicationproxy.md)

