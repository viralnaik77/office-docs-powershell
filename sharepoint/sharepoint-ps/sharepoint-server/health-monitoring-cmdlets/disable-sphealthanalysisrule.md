---
title: "Disable-SPHealthAnalysisRule"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2553a88c-3146-437c-9971-7fb162d42531

description: "Disables health analyzer rules."
---

# Disable-SPHealthAnalysisRule

Disables health analyzer rules.
  
```
Disable-SPHealthAnalysisRule [-Identity] <SPHealthAnalysisRuleInstancePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Disable-SPHealthAnalysisRule** cmdlet to disable a health analyzer rule. 
  
> [!NOTE]
> The SPHealthAnalysisRule cmdlets were first introduced in the February 2011 Cumulative Update, which is available for download as follows: > --[Description of the SharePoint Foundation 2010 Cumulative Update Server Hotfix Package (SharePoint Foundation server-package)](https://support.microsoft.com/kb/2475880)> --[Description of the SharePoint Server 2010 Cumulative Update Server Hotfix Package (MOSS server-package](https://support.microsoft.com/kb/2475878)
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPHealthAnalysisRuleInstancePipeBind  <br/> |Specifies the name or GUID of the health analyzer rule to disable.  <br/> The type must be a valid name; an instance of a valid **SPHealthAnalysisRule** object, or a valid GUID (for example, 12345678-90ab-cdef-1234-567890bcdefgh).  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## Example

---------------------EXAMPLE 1---------------------------
  
```
Disable-SPHealthAnalysisRule -Identity "CustomRule"
```

This example disables the health analyzer rule named CustomRule.
  
## See also

#### 

[Enable-SPHealthAnalysisRule](enable-sphealthanalysisrule.md)
  
[Get-SPHealthAnalysisRule](get-sphealthanalysisrule.md)

