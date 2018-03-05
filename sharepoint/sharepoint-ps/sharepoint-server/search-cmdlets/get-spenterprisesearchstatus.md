---
title: "Get-SPEnterpriseSearchStatus"
ms.author: tlarsen
author: tlarsen
manager: laurawi
ms.date: 11/29/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb0f69b-2ed1-4bf4-b461-2895da6f9ef0

description: "Retrieves diagnostics information for the search components."
---

# Get-SPEnterpriseSearchStatus

Retrieves diagnostics information for the search components.
  
```
Get-SPEnterpriseSearchStatus -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Component <String>] [-Constellation <SwitchParameter>] [-Detailed <SwitchParameter>] [-DetailSearchRuntime <SwitchParameter>] [-HealthReport <SwitchParameter>] [-JobStatus <SwitchParameter>] [-Primary <SwitchParameter>] [-Text <SwitchParameter>]

```

## Example

------------------EXAMPLE 1------------------
  
```
Get-SPEnterpriseSearchServiceApplication | Get-SPEnterpriseSearchStatus -Text
```

This example retrieves diagnostics information about all search components of the default Search Service Application.
  
------------------EXAMPLE 2------------------
  
```
Get-SPEnterpriseSearchStatus -SearchApplication "Search Service Application" -JobStatus -Text
```

This example retrieves the background activity job status for the search analytics timer jobs.
  
------------------EXAMPLE 3------------------
  
```
Get-SPEnterpriseSearchServiceApplication | Get-SPEnterpriseSearchStatus -HealthReport -Component IndexComponent1 -Text
```

This example retrieves the diagnostic information for the index component named  `IndexComponent1`.
  
## Detailed Description

This cmdlet retrieves diagnostic information for all or specified search components in the active topology of a Search Service Application.
  
If you don't specify any of the optional parameters, the cmdlet will retrieve the health status of all the search components within the Search Service Application. Each search component will have one of the following states:
  
- Active: The search component is running OK
    
- Degraded: The search component is in a status where it cannot perform all operations correctly. The reason for the degraded status is typically a transient situation related to a restart or network issues.
    
- Failed: The search component is not running. This status indicated that the component cannot perform operations correctly.
    
- Unknown: The component can't be reached. The reason for the unknown status is typically hardware or communication issues.
    
If you have defined more than one Index component for a partition in your search topology, this cmdlet will indicate which index component that has the Primary role for this partition.
  
You can use the cmdlet to output the following additional information:
  
- List the status of background activities (batch jobs) initiated by the search components
    
- List detailed diagnostic information for the index component
    
- Debug information that may be used by Microsoft for detailed issue resolution
    
If you don't want to iterate over the output in a script, use the  *Text*  parameter. If you do not use the  *Text*  parameter, the cmdlet will output a set of objects that have the following properties: 
  
- string Name: the name of a search component, a health report item or a constellation property
    
- string State: the status of the search component
    
- string Level: when you are using the  *HealthReport*  parameter, this property indicates the importance level of each health report item (Error, Warning, Info, Verbose) 
    
- string Message: additional information that is provided as a text string
    
- ReadOnlyDictionary\<string,string\>Details: dictionary name/value pairs that provide additional diagnostic information
    
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _SearchApplication_ <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> |Specifies the search service application that contains the search components.  <br/> |
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _Component_ <br/> |Optional  <br/> |System.String  <br/> |Specifies the name of the search component. This parameter is only used in association with the  *HealthReport*  and  *Primary*  parameter.  <br/> |
| _Constellation_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if internal diagnostic information for the search topology should be provided. This parameter should only be used for debugging.  <br/> |
| _Detailed_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies the level of detail for the  *HealthReport*  parameter. When this parameter is used, the cmdlet will also output verbose diagnostic information.  <br/> |
| _DetailSearchRuntime_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if internal diagnostic information for the search runtime should be provided. This parameter should only be used for debugging.  <br/> |
| _HealthReport_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if diagnostic information for the search component should be provided. When using this parameter, you must specify the component name using the **Component** parameter.  <br/> |
| _JobStatus_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if status information for the **Search Analytics** and **Usage Analytics** timer jobs should be provided.  <br/> |
| _Primary_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if the Admin component has the Primary role. When using this parameter, you must specify the component name using the **Component** parameter. Returns true if the Admin Component has the Primary role.  <br/> |
| _Text_ <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Specifies if the print output from this cmdlet should be outputted in a format that is convenient for reading. If not used, this cmdlet outputs a SearchStatusInfo object.  <br/> When using this parameter, the output is printed to the console and cannot be piped to a file or another program.  <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**SearchApplication** <br/> |Required  <br/> |Microsoft.Office.Server.Search.Cmdlet.SearchServiceApplicationPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Component** <br/> |Optional  <br/> |System.String  <br/> ||
|**Constellation** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Detailed** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DetailSearchRuntime** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**HealthReport** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**JobStatus** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Primary** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**Text** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   

