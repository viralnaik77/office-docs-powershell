---
title: "Use Microsoft PowerShell to administer SharePoint Server"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 8/9/2017
ms.audience: ITPro
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: ae4901b4-505a-42a9-b8d4-fca778abc12e
description: "Summary: Learn about basic Microsoft PowerShell cmdlets and concepts and how to use Microsoft PowerShell with SharePoint Server 2013 and SharePoint Server."
---

# Use Microsoft PowerShell to administer SharePoint Server

 **Summary:** Learn about basic Microsoft PowerShell cmdlets and concepts and how to use Microsoft PowerShell with SharePoint Server 2013 and SharePoint Server. 
  
In this article:
  
- [Overview](#section1)
    
- [Accessing PowerShell for SharePoint Server](use-microsoft-powershell-to-administer-sharepoint-server.md#section2)
    
- [Permissions](#section3)
    
- [Scripts and execution policies](#sectionExPol)
    
- [Learning PowerShell](#section4)
    
## Overview
<a name="section1"> </a>

Microsoft PowerShell is a command-line shell and scripting language that provides an administrator full access to applicable application programming interfaces (APIs). Administrators can interact directly with SharePoint Server to manipulate web applications, site collections, sites, lists and much more. In addition, an administrator can script cmdlets (pronounced "command-lets").
  
 By default, Powershell is located at the following path: \<%SystemRoot%\>\System32\WindowsPowerShell\v1.0\PowerShell.exe. 
  
## Accessing PowerShell for SharePoint Server
<a name="section2"> </a>

After you install SharePoint Server, applicable PowerShell cmdlets are available in the SharePoint 2016 Management Shell. You can manage most aspects of SharePoint Server in the SharePoint Management Shell. You can create new site collections, web applications, user accounts, service applications, proxies, and more. Commands that you type in the SharePoint Management Shell return SharePoint objects that are based on the Microsoft .NET Framework. You can apply these objects as input to subsequent commands or store the objects in local variables for later use.
  
With the SharePoint Management Shell, you do not have to register the snap-in that contains the cmdlets. Registration of the Microsoft.SharePoint.PowerShell.dll module for SharePoint Server cmdlets is automatic, as a result of the  `Add-PSSnapin Microsoft.SharePoint.PowerShell` line in the SharePoint.ps1 file that is located in  _%CommonProgramFiles%_\Microsoft Shared\Web Server Extensions\16\Config\PowerShell\Registration. To use the PowerShell console, you must register this snap-in manually.
  
> [!NOTE]
> For SharePoint 2013, registration of the .ps1 file is located in  _%CommonProgramFiles%_\Microsoft Shared\Web Server Extensions\15\Config\PowerShell\Registration 
  
Whether you use the SharePoint Management Shell or the PowerShell console, you can also load additional snap-ins. For more information, see [Customizing Profiles](https://go.microsoft.com/fwlink/p/?LinkId=183166).
  
### To access the SharePoint Management Shell

- Start the SharePoint Management Shell.
    
> [!NOTE]
> The SharePoint Management Shell and the PowerShell console also differ in the use of the  `ReuseThread` option, which defines how the threading model is used. The SharePoint Management Shell's use is defined by this line,  `{Host.Runspace.ThreadOptions = "ReuseThread"}`, which is in the SharePoint.ps1 file. For more information, see [PS Thread Options](https://go.microsoft.com/fwlink/p/?LinkId=183145). 
  
## Permissions
<a name="section3"> </a>

### On-Premises

 Before you can use the **Add-SPShellAdmin** cmdlet to grant permissions for users to run SharePoint Server cmdlets, verify that you meet all of the following minimum requirements: 
  
- You must have membership in the **securityadmin** fixed server role on the SQL Server instance 
    
- You must have membership in the **db_owner** fixed database role on all databases that are to be updated. 
    
- You must be a member of the Administrators group on the server on which you are running the PowerShell cmdlet.
    
> [!NOTE]
> If these permissions are not satisfied, contact your Setup administrator or SQL Server administrator to request these permissions. 
  
For additional information about PowerShell permissions, see [Permissions](use-microsoft-powershell-to-administer-sharepoint-server.md#section3) and [Add-SPShellAdmin](microsoft-powershell-for-sharepoint-server-reference/security-cmdlets/add-spshelladmin.md)
  
If you do not have membership in the **SharePoint_Shell_Access** role or **WSS_Admin_WPG** local group, use the **Add-SPShellAdmin** cmdlet to add the **WSS_Admin_WPG** group in all front-end web servers in the SharePoint farm and the **SharePoint_Shell_Access** role. If the SQL Server database does not have a **SharePoint_Shell_Access** role, the role is automatically created when you run the **Add-SPShellAdmin** cmdlet. After you run the **Add-SPShellAdmin** cmdlet, users can run SharePoint PowerShell cmdlets in a multiple-server farm environment. 
  
> [!NOTE]
>  When you install SharePoint Server, the user account from which you run the installation is granted the appropriate permissions to run PowerShell cmdlets. If any users have not been added to run a PowerShell cmdlet, you can use the **Add-SPShellAdmin** cmdlet to add them. 
  
You must run the **Add-SPShellAdmin** cmdlet for all databases to which you want to grant access. If no database is specified, the farm configuration database is used. If you do specify a database, the farm content database will be included in addition to the farm configuration database that you specify. 
  
To see a list of all of the **SPShellAdmin** cmdlets, from a PowerShell command prompt, type  `Get-Command -Noun SPShellAdmin`.
  
### SharePoint Online

Verify that you have the following administrative permissions:
  
- You must be assigned the global administrator role on the SharePoint Online site on which you are running the PowerShell cmdlet. For more information, see [Default administrative roles and user groups](https://go.microsoft.com/fwlink/p/?LinkId=242451).
    
    > [!IMPORTANT]
    > You can use a specific group of PowerShell with SharePoint Online. For more information, see [Windows PowerShell for SharePoint Online](http://technet.microsoft.com/library/0720676d-cee9-4cec-be2b-cb5eb0e7e952.aspx). 
  
## Scripts and execution policies
<a name="sectionExPol"> </a>

Although you can use Microsoft PowerShell to perform a single administrative task, you can also use a script to automate a series of tasks. A script is a text file that contains one or more Microsoft PowerShell commands. Microsoft PowerShell scripts have a .ps1 file name extension. 
  
To run scripts, the minimum required execution policy for SharePoint Server is RemoteSigned, although the default policy for PowerShell is Restricted. If the policy is left as Restricted, the SharePoint Management Shell will change the policy for PowerShell to RemoteSigned. This means that you must select **Run as administrator** to start the SharePoint 2016 Management Shell with elevated administrative permission. This change will apply to all PowerShell sessions. For more information, see [ExecutionPolicy Enumeration](https://go.microsoft.com/fwlink/p/?LinkId=242452).
  
For additional information about scripts and execution policies, see [about_scripts](https://go.microsoft.com/fwlink/p/?LinkId=144310) and [about_Execution_Policies](https://go.microsoft.com/fwlink/p/?LinkId=193050) respectively. 
  
## Learning PowerShell
<a name="section4"> </a>

There are several PowerShell learning resources for SharePoint IT professionals.
  
 **TechNet Scripting Center**
  
The TechNet Scripting Center includes many resources to help you learn the basics about PowerShell. It also contains script repositories with samples of scripts that are typically used with various Microsoft products. The following table shows the main learning resources.
  
|**Page**|**Description**|
|:-----|:-----|
|[Windows PowerShell Documentation on TechNet](https://go.microsoft.com/fwlink/p/?LinkId=187813) <br/> |This section of the TechNet Library contains web copies of the core PowerShell Get-Help topics. The section also has web copies of the PowerShell Getting Started document, the PowerShell.exe help, and a PowerShell primer.  <br/> |
|[Scripting With Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=187815) <br/> |The home page for PowerShell scripting learning resources.  <br/> |
|[Windows PowerShell Owner's Manual](https://go.microsoft.com/fwlink/p/?LinkId=187817) <br/> |Web-based guide for getting started with PowerShell.  <br/> |
|[Windows PowerShell Quick Reference](https://go.microsoft.com/fwlink/p/?LinkId=187819) <br/> |Downloadable copy of the Quick Reference document that is installed with PowerShell.  <br/> |
   
As you read these resources, consider that the following concepts and cmdlets are useful ones to learn before you use PowerShell for SharePoint Server:
  
- [Get-Command](https://go.microsoft.com/fwlink/p/?LinkId=171069)
    
- [Get-Member](https://go.microsoft.com/fwlink/p/?LinkId=171070)
    
- [Get-Help](https://go.microsoft.com/fwlink/p/?LinkId=171068)
    
- [Aliasing](https://go.microsoft.com/fwlink/p/?LinkId=113207)
    
- [Piping and the Pipeline in Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=187808)
    
- [Cmdlet Parameter Sets](https://go.microsoft.com/fwlink/p/?LinkId=187810)
    
- [Foreach-Object](https://go.microsoft.com/fwlink/p/?LinkId=187812)
    
- [Where-Object](https://go.microsoft.com/fwlink/p/?LinkId=187811)
    

