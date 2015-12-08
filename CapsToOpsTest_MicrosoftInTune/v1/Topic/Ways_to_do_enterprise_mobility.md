---
description: na
search: na
title: Ways to do enterprise mobility
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-17
ms.author: 2acc2e0c-a3ea-42a3-8a95-f1f50c2bbe2f
---
# Ways to do enterprise mobility
Microsoft provides several options for managing your mobile devices. We’ve provided information on this page to help you decide between these different options for meeting your enterprise mobility needs:

- [Choose between Intune and MDM for Office 365](#BKMK_MDMOfferings)

- [Choose between Intune by itself or integrating Intune with System Center Configuration Manager](#BKMK_HybridOfferings)

## <a name="BKMK_MDMOfferings"></a>Choose between Intune and MDM for Office 365

|Consideration <br /> <br />|MDM for Office 365 <br /> <br />|[!INC[wit_firstref](../Token/wit_firstref_md.md)] <br /> <br />|
|-----------------|----------------------|---------------------------------------------------------|
|Cost <br /> <br />|Included with many [Office 365 commercial subscriptions](http://products.office.com/business/enterprise-productivity-tools). <br /> <br />|Requires a [paid subscription for Microsoft Intune](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/Purchasing.aspx) or can be purchased with the [Enterprise Mobility Suite](http://www.microsoft.com/en-us/server-cloud/products/enterprise-mobility-suite/Purchasing.aspx). <br /> <br />|
|How you manage devices <br /> <br />|Manage devices using the [Office 365 admin center](https://support.office.com/article/About-the-Office-365-admin-center-58537702-d421-4d02-8141-e128e3703547). <br /> <br />|If you use [!INC[wit_nextref](../Token/wit_nextref_md.md)] by itself, you manage devices using the [Intune admin console](https://technet.microsoft.com/library/dn646966.aspx). <br /> <br />If you integrate Intune with System Center 2012 Configuration Manager, you use the Configuration Manager console to manage devices on-premises and in the cloud. <br /> <br />|
|Devices you can manage <br /> <br />|Cloud-based management for: <br /> <br /><ul><li>iOS </li><li>Android </li><li>Windows Phone </li> </ul>|Cloud-based management for: <br /> <br /><ul><li>iOS </li><li>Mac OS X </li><li>Android </li><li>Windows Phone </li><li>Windows PCs </li> </ul>|
|Key capabilities <br /> <br />|<ul><li>Ensure that Office 365 corporate email and documents can be accessed only on phones and tablets that are managed by your company and that are compliant with your IT policies. </li><li>Set and manage security policies, like device level pin lock and jailbreak detection, to help prevent unauthorized users from accessing corporate email and data on a device when it is lost or stolen. </li><li>Remove Office 365 company data from an employee’s device while leaving their personal data in place. </li> </ul>For the latest information about Office 365 MDM capabilities, see [capabilities of Built-in Mobile Device Management for Office 365](https://technet.microsoft.com/library/ms.o365.cc.devicepolicysupporteddevice.aspx). <br /> <br />|MDM for Office 365 capabilities, plus: <br /> <br /><ul><li>Help users securely access corporate resource with certificates, Wi-Fi, VPN, and email profiles. </li><li>Enroll and manage collections of corporate-owned devices, simplifying policy and app deployment. </li><li>Deploy your internal line-of-business apps and apps in stores to users. </li><li>Enable your users to securely access corporate information using the Office mobile and line-of business apps they know, while ensuring security of data by restricting actions like *copy*, *cut*, *paste*, and *save as*, to only those apps managed by [!INC[wit_nextref](../Token/wit_nextref_md.md)]. </li><li>Enable secure web browsing using the [!INC[wit_nextref](../Token/wit_nextref_md.md)] Managed Browser app. </li><li>Manage PC's from the cloud with no infrastructure required using [!INC[wit_nextref](../Token/wit_nextref_md.md)], or connect [!INC[wit_nextref](../Token/wit_nextref_md.md)] to [!INC[cm5short](../Token/cm5short_md.md)] to manage all of your devices including PCs, Macs, Linux and UNIX servers, and mobile devices from a single management console. </li> </ul>|
Starting in October 2015, administrators can manage users and their mobile devices using both Intune and Office 365 concurrently on the same tenant. This lets you decided which solution is the best solution for specific users and their corresponding devices. You can then specify whether a user and his or her devices are managed with Office 365 MDM or the more feature-rich Intune management solution.

## <a name="BKMK_HybridOfferings"></a>Choose between Intune by itself or integrating Intune with System Center Configuration Manager

|You might choose [!INC[wit_nextref](../Token/wit_nextref_md.md)] stand-alone if: <br /> <br />|You might choose [!INC[wit_nextref](../Token/wit_nextref_md.md)] + Configuration Manager if: <br /> <br />|
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
|<ul><li>You want to manage mobile devices </li><li>You want to manage computers that are not joined to a domain </li><li>You have fewer than 50,000 devices to manage </li><li>You have no (or limited) on-premises IT infrastructure **Note:**    [!INC[wit_nextref](../Token/wit_nextref_md.md)] does not require on-premises IT infrastructure, however it can use the capabilities of Exchange ActiveSync or Active Directory Domain Services if you have those installed. </li><li>You have a mobile or highly distributed workforce. Cloud-based device management lets you manage mobile devices and computers anywhere in the world. </li> </ul>|<ul><li>You want to manage computers joined to a domain. </li><li>You want to manage servers. </li><li>You want to manage computers with the Configuration Manager client, Mac computers, Linux and UNIX server, and mobile devices enrolled with Intune from the same console. </li><li>You have more than 50,000 devices to manage. </li><li>You have on-premises IT infrastructure in place, or plan to deploy such infrastructure. In this configuration, the device and resource management experience is fully unified. </li><li>User names and passwords are synchronized, providing users with a single account that they use to access company resources, whether from a domain-joined computer or from a mobile device. </li> </ul>|

### Detailed comparison of capabilities
The following tables compare the device and app management capabilities available to you when you use [!INC[wit_nextref](../Token/wit_nextref_md.md)] alone, Configuration Manager alone, or a solution that uses both products.

To learn more about using Configuration Manager with [!INC[wit_nextref](../Token/wit_nextref_md.md)], see [Manage Mobile Devices with Configuration Manager and Microsoft Intune](http://msdn.microsoft.com/en-us/library/2c6bd0e5-d436-41c8-bf38-30152d76be10).

#### Device support

|Platform <br /> <br />|[!INC[wit_firstref](../Token/wit_firstref_md.md)] <br /> <br />|System Center 2012 Configuration Manager SP2 <br /> <br />|System Center 2012 Configuration Manager SP2 and [!INC[wit_nextref](../Token/wit_nextref_md.md)] <br /> <br />|
|------------|---------------------------------------------------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------|
|Microsoft Windows <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Microsoft Windows Server <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Windows Phone <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|Windows RT <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|iOS <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|Android and Samsung KNOX <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|Mac OS X <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Unix/Linux servers <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|

#### Product capabilities
> [!TIP]
> Where indicated with (R2), the listed capability requires Microsoft System Center 2012 R2 Configuration Manager or later.

|Scenario <br /> <br />|[!INC[wit_firstref](../Token/wit_firstref_md.md)] <br /> <br />|System Center 2012 Configuration Manager SP2 <br /> <br />|System Center 2012 Configuration Manager SP2 and [!INC[wit_nextref](../Token/wit_nextref_md.md)] <br /> <br />|
|------------|---------------------------------------------------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------|
|**Compliance Settings** <br /> <br />||||
|Deploy and customize Windows PC device configuration settings (e.g., WMI, registry) <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Deploy and customize Mac OS X configuration settings <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Deploy configuration settings to mobile devices. <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Deploy custom mobile device settings (such as OMA-URI and Apple Configurator) <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Deployment** <br /> <br />||||
|Deploy apps to devices and Windows PCs <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Deploy Windows operating systems <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Security and Privacy** <br /> <br />||||
|Manage Windows software updates <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Monitor malware on Windows PCs with Endpoint Protection <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Administration and Reporting** <br /> <br />||||
|Monitor and report on how often software is being used with software metering <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Hardware and software inventory <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Extend hardware and software inventory for Windows PCs <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Use role-based administration and reporting to control who has access to product capabilites <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Run reports for Windows PCs and enrolled mobile devices from the same console <br /> <br />|No <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|Customize existing reports, and write your own reports using SQL Server Reporting Services <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Data Protection for mobile devices** <br /> <br />||||
|Deploy security settings to mobile devices <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Remote wipe <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Remote lock <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Passcode reset <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Company resource access** <br /> <br />||||
|Email profiles <br /> <br />|Yes <br /> <br />|Yes (R2) <br /> <br />|Yes (R2) <br /> <br />|
|Wi-Fi profiles <br /> <br />|Yes <br /> <br />|Yes (R2) <br /> <br />|Yes (R2) <br /> <br />|
|VPN profiles <br /> <br />|Yes <br /> <br />|Yes (R2) <br /> <br />|Yes (R2) <br /> <br />|
|Certificate profiles <br /> <br />|Yes <br /> <br />|Yes (R2) <br /> <br />|Yes (R2) <br /> <br />|
|Manage access to Exchange email and SharePoint with conditional access <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Mobile application management <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|App compliance policies (compliant and noncompliant apps) <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Kiosk mode <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Managed Internet browser policy <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Automation** <br /> <br />||||
|Use PowerShell to automate operations <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|

## See Also
[Introduction to Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)

