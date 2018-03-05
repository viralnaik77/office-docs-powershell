---
title: "InfoPath Services cmdlets in SharePoint Server 2016"
ms.author: kirks
author: Techwriter40
manager: laurawi
ms.date: 2/25/2016
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: 68d913c8-fb32-4a3f-96ac-b1444ddb76d5
description: "Summary: Lists Windows PowerShell cmdlets that help you manage InfoPath Forms Services in a SharePoint Server 2016 farm."
---

# InfoPath Services cmdlets in SharePoint Server 2016

 **Summary:** Lists Windows PowerShell cmdlets that help you manage InfoPath Forms Services in a SharePoint Server 2016 farm. 
  
InfoPath Forms Services is a service in SharePoint Server 2016 that you can use to view, edit, and configure a form template in InfoPath 2016 or viewed within a Web browser. 
  
All InfoPath Forms Services settings will support backup and recovery regardless of whether there is a UI setting in the Central Administration Web site. However, backup and recovery only apply to the service and administrative-level settings; end-user content is not backed up as part of this process.
  
[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md) includes a complete list of all cmdlets in SharePoint Server 2016. 
  
|**Cmdlet name**|**Description**|
|:-----|:-----|
|**[Add-SPInfoPathUserAgent](add-spinfopathuseragent.md)** <br/> |Adds a user agent to a farm.  <br/> |
|**[Disable-SPInfoPathFormTemplate](disable-spinfopathformtemplate.md)** <br/> |Deactivates an InfoPath 2016 form template from the specified site collection.  <br/> |
|**[Enable-SPInfoPathFormTemplate](enable-spinfopathformtemplate.md)** <br/> |Activates an InfoPath 2016 form template in the specified site collection.  <br/> |
|**[Export-SPInfoPathAdministrationFiles](export-spinfopathadministrationfiles.md)** <br/> |Saves InfoPath 2016 form templates on the SharePoint Central Administration Web site and .udcx files to a .cab file.  <br/> |
|**[Get-SPDataConnectionFile](get-spdataconnectionfile.md)** <br/> |Returns a data connection file or a collection of data connection files.  <br/> |
|**[Get-SPDataConnectionFileDependent](get-spdataconnectionfiledependent.md)** <br/> |Returns deployed forms on the server dependent on a universal data connection.  <br/> |
|**[Get-SPInfoPathFormsService](get-spinfopathformsservice.md)** <br/> |Returns the InfoPath Forms Services in SharePoint Server 2013 settings that are in the farm.  <br/> |
|**[Get-SPInfoPathFormTemplate](get-spinfopathformtemplate.md)** <br/> |Returns an InfoPath 2016 form template.  <br/> |
|**[Get-SPInfoPathUserAgent](get-spinfopathuseragent.md)** <br/> |Returns a user agent or all the currently defined user agents for the farm.  <br/> |
|**[Get-SPInfoPathWebServiceProxy](get-spinfopathwebserviceproxy.md)** <br/> |Returns the Web proxy settings for the Web application.  <br/> |
|**[Import-SPInfoPathAdministrationFiles](import-spinfopathadministrationfiles.md)** <br/> |Imports InfoPath 2016 form templates and .udcx files that are located on the SharePoint Central Administration Web site.  <br/> |
|**[Install-SPDataConnectionFile](install-spdataconnectionfile.md)** <br/> |Installs the provided data connection file.  <br/> |
|**[Install-SPInfoPathFormTemplate](install-spinfopathformtemplate.md)** <br/> |Installs an InfoPath 2016 form template on a farm.  <br/> |
|**[Remove-SPInfoPathUserAgent](remove-spinfopathuseragent.md)** <br/> |Removes a user agent.  <br/> |
|**[Set-SPDataConnectionFile](set-spdataconnectionfile.md)** <br/> |Sets properties of a data connection file.  <br/> |
|**[Set-SPInfoPathFormsService](set-spinfopathformsservice.md)** <br/> |Sets parameters for InfoPath Forms Services in SharePoint Server 2013.  <br/> |
|**[Set-SPInfoPathFormTemplate](set-spinfopathformtemplate.md)** <br/> |Sets properties of an InfoPath 2016 form template.  <br/> |
|**[Set-SPInfoPathWebServiceProxy](set-spinfopathwebserviceproxy.md)** <br/> |Sets parameters for an existing SharePoint Web service application.  <br/> |
|**[Start-SPInfoPathFormTemplate](start-spinfopathformtemplate.md)** <br/> |Activates a previously quiesced InfoPath 2016 form template.  <br/> |
|**[Stop-SPInfoPathFormTemplate](stop-spinfopathformtemplate.md)** <br/> |Disables an InfoPath 2016 form template on a farm before an upgrade.  <br/> |
|**[Test-SPInfoPathFormTemplate](test-spinfopathformtemplate.md)** <br/> |Validates that an InfoPath 2016 form template is browser-enabled.  <br/> |
|**[Uninstall-SPDataConnectionFile](uninstall-spdataconnectionfile.md)** <br/> |Removes a data connection file.  <br/> |
|**[Uninstall-SPInfoPathFormTemplate](uninstall-spinfopathformtemplate.md)** <br/> |Removes an InfoPath 2016 form template from a farm.  <br/> |
|**[Update-SPInfoPathUrl](http://technet.microsoft.com/library/3fd3e3b6-429a-40f3-bd33-7d7733630ba1.aspx)** <br/> |Updates InfoPath 2016 form templates (.xsn files) and universal data connections (.udcx files), including all .xsn files and .udcx files that were deployed by an administrator.  <br/> |
|**[Update-SPInfoPathFormTemplate](update-spinfopathformtemplate.md)** <br/> |Upgrades all InfoPath 2016 form templates on the farm.  <br/> |
|**[Update-SPInfoPathUserFileUrl](update-spinfopathuserfileurl.md)** <br/> |Updates InfoPath form templates (.xsn files) and universal data connections (.udcx files).  <br/> |
   
## See also

#### 

[Index of MicrosoftPowerShell cmdlets for SharePoint Server](../../../docs-conceptual/sharepoint-server/index-of-microsoftpowershell-cmdlets.md)

