---
title: "Get-SPHealthAnalysisRule"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 12/20/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 209a2e6a-9547-46a8-accf-7a8206b8e6e3

description: "Gets a health analyzer rule."
---

# Get-SPHealthAnalysisRule

Gets a health analyzer rule.
  
```
Get-SPHealthAnalysisRule [-AssignmentCollection <SPAssignmentCollection>]
```

## Detailed Description

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/?LinkID=187810).
  
Use the **Get-SPHealthAnalysisRule** cmdlet to return a list of a health analyzer rules. To return a specify health analyzer rule, use the **Identity** parameter; otherwise, all health analyzer rules will be returned. 
  
The SPHealthAnalysisRule cmdlets were first introduced in the February 2011 Cumulative Update, which is available for download as follows: 
  
--[Description of the SharePoint Foundation 2010 Cumulative Update Server Hotfix Package (SharePoint Foundation server-package)](https://support.microsoft.com/kb/2475880)
  
--[Description of the SharePoint Server 2010 Cumulative Update Server Hotfix Package (MOSS server-package](https://support.microsoft.com/kb/2475878)
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPHealthAnalysisRuleInstancePipeBind  <br/> |Specifies the name or GUID of the health analyzer rule to get.  <br/> The type must be a valid name, an instance of a valid **SPHealthAnalysisRule** object, or a valid GUID (for example, 12345678-90ab-cdef-1234-567890bcdefgh).  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
   
## Example

---------------------EXAMPLE 1---------------------------
  
```
Get-SPHealthAnalysisRule -Identity "CustomRule"
```

This example returns the health analyzer rule named CustomRule.
  
## See also

#### 

[Disable-SPHealthAnalysisRule](disable-sphealthanalysisrule.md)
  
[Enable-SPHealthAnalysisRule](enable-sphealthanalysisrule.md)

