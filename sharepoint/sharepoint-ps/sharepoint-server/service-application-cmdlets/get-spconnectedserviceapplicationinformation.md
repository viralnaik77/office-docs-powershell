---
title: "Get-SPConnectedServiceApplicationInformation"
ms.author: kirks
author: Techwriter40
ms.date: 11/23/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2155e83f-ba22-4b53-b356-79f8219febe4

description: "Returns the health of the service application proxy."
---

# Get-SPConnectedServiceApplicationInformation

Returns the health of the service application proxy.
  
```
Get-SPConnectedServiceApplicationInformation [-AssignmentCollection <SPAssignmentCollection>] [-ServiceApplicationProxy <SPServiceApplicationProxyPipeBind>]

```

## Example

------------------EXAMPLE-----------------------
  
```
$validProxy = $false
```

```
$upaProxy = Get-SPServiceApplicationProxy | where{$_.TypeName -eq "User Profile Service Application Proxy"}
```

```
$proxyHealth = Get-SPConnectedServiceApplicationInformation -ServiceApplicationProxy $upaProxy 
```

```
    if(($proxyHealth -ne $null) -and ($proxyHealth.ApplicationAddressesState -eq "UpToDate"))
     {
         $validProxy = $true
     }
     else
     {
       $validProxy = $false 
     }

```

This example checks the health of the service application proxy server.
  
## Detailed Description

The **Get-SPConnectedServiceApplicationInformation** cmdlet checks whether the proxy to a service application is in good health. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715). 
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _AssignmentCollection_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
| _ServiceApplicationProxy_ <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPServiceApplicationProxyPipeBind  <br/> |Specifies the name of the service application proxy.  <br/> |
   

