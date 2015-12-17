---
description: na
keywords: na
pagetitle: Microsoft Intune features
search: na
ms.date: 4/24/2015 8:00:00 AM
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 118a36f6-02c6-4e99-9c72-0b9daddc3b03
ms.author: 03258b9b-2cea-4654-ab05-a27214174f4b
robots: noindex,nofollow
---
# Microsoft Intune features
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] provides a cloud-based service that can help your business protect and manage devices. Because it is cloud-based, it can be administered from any Silverlight-enabled web browser. [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] can manage:

- **Mobile devices** (including phones and tablets running Android, iOS, Windows Phone and Windows RT operating systems). Computers running Windows 8.1 can be managed as mobile devices, or can be managed as computers using the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] client software.

- **Computers** running a professional edition of Windows Vista, Windows 7, Windows 8 or Windows 8.1.

For more information on mobile devices and computers that you can manage with [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], see [Mobile device management capabilities in Microsoft Intune](../Topic/Mobile_device_management_capabilities_in_Microsoft_Intune.md) and [Windows PC management capabilities in Microsoft Intune](../Topic/Windows_PC_management_capabilities_in_Microsoft_Intune.md).

This evaluation guide covers the following:

- [Intune capabilities](../Topic/Microsoft_Intune_features.md#WIT_Cap)

- [Microsoft Intune administration](../Topic/Microsoft_Intune_features.md#WIT_Adm)

- [Microsoft Intune free trial and pricing](../Topic/Microsoft_Intune_features.md#WIT_Fre)

## <a name="WIT_Cap"></a>Intune capabilities
**General capabilities:**

- **Manage mobile devices and computers, no servers or intranet required.** You can manage mobile devices and computers, even if those devices are not joined to a domain or brought on-site. This makes [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ideal for a company with a mobile or geographically-distributed workforce.

- **Require encryption of mobile devices and computers.** Mobile devices that support encryption can be required to use it. You can also require computers that support Bitlocker drive encryption to use it. If a mobile device or computer with encryption is lost or stolen, the data on the device’s storage media is unreadable, helping to secure that data it from theft.

- **Generate hardware and software inventories and reports.** You can gather information on the hardware and software used by your company, helping you to plan your hardware upgrade cycle or determine if unwanted software is installed on managed devices.

- **Monitor mobile devices and computers.** You can create alerts to notify you when there is a problem with a mobile device or a computer, and also have alerts trigger e-mail notifications so that the right people are informed of the problem.

- **Provide a “self-service” model for IT.** Users can use the company portal to enroll devices, to install site-licensed software, or to find contact information for IT administrators.

- **Support multi-factor authentication.** [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] now supports multi-factor authentication. For details, see [Protect Windows devices with multi-factor authentication in Microsoft Intune](../Topic/Protect_Windows_devices_with_multi-factor_authentication_in_Microsoft_Intune.md).

- **Available in multiple languages.** Intune is now available in the following languages:

   - Chinese (Simplified and Traditional)

   - Czech

   - Danish

   - Dutch

   - English

   - Finnish

   - French

   - German

   - Greek

   - Hungarian

   - Italian

   - Japanese

   - Korean

   - Norwegian

   - Polish

   - Portuguese

   - Romanian

   - Russian

   - Spanish

   - Swedish

   - Turkish

For a list of the countries where the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] service is supported, see [International availability](https://products.office.com/en-us/business/international-availability).

**Mobile device management (MDM) capabilities:**

- **Configure passwords.** Password management differs across mobile device platforms, but all supported platforms allow you to require a password, limit the number of failed sign-in attempts, limit the minutes of activity before the screen locks, set the time for password expiration, and prevent the use of previously-used passwords.

- **Control system and cloud storage settings for mobile devices.** These differ across mobile device platforms, but highlights include the ability to block the iOS lock screen notifications view (to keep meeting details confidential), and the ability to collect diagnostic data from Windows Phone 8.1 and iOS devices.

- **Manage e-mail access for mobile devices using Exchange ActiveSync.** You can control e-mail access settings such as whether devices can download attachments, or how much of an e-mail folder is synchronized with a mobile device.

- **Application settings.** You can control browser settings, and also such application settings as whether app stores can be used on mobile devices.

- **Device capabilities, cellular and voice.** You can allow or deny the use of a camera, control roaming settings, and enable or disable iOS voice assistant and voice dialing features.

- **Reset passcodes, lock or wipe.** You can reset passcodes if users lose access to their device, lock missing or stolen devices, or even wipe data off of missing or stolen devices.

- **Certificate, email, VPN and Wifi profiles.** You can deploy certificate profiles to mobile devices, and also deploy e-mail, VPN and Wifi profiles. See [Enable access to company resources with Microsoft Intune](http://msdn.microsoft.com/en-us/library/5b090c5a-6f12-4e60-ace0-c9929afaa9a3).

- **Manage corporate-owned iOS devices.** You can set up devices for enrollment and then distribute them to specific users, or you can enroll devices so that they can be shared by multiple users. See [Enroll corporate-owned iOS devices in Microsoft Intune](../Topic/Enroll_corporate-owned_iOS_devices_in_Microsoft_Intune.md).

- **Mobile application management.** Managed mobile apps can be configured to restrict certain app operations, such as copy and paste, to help protect your organization’s data. You can also use the managed browser to control the sites that users are allowed to visit. See [Configure and deploy mobile application management policies in the Microsoft Intune console](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md) and [Manage Internet access using managed browser policies with Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md).

- **Conditional access.** Use [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] conditional access policies to control access to on-premises Microsoft Exchange email from mobile devices, even when the device is not managed by Intune. See [Manage access to email and SharePoint with Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md).

For a complete list of MDM capabilities, see [Mobile device management capabilities in Microsoft Intune](../Topic/Mobile_device_management_capabilities_in_Microsoft_Intune.md).

**Intune computer management capabilities:**

- **Manage software updates.** You can keep computers up-to-date, and manage when updates are applied.

- **Set Windows firewall policy.** This helps to ensure that no computer used by your company has an inactive or improperly-configured firewall.

- **Anti-malware protection.**[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] includes [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Endpoint Protection, and allows you to set policies to ensure that computers are kept up-to-date with the latest anti-malware definition updates.

- **Remote assistance.**[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] allows users to contact IT support staff, who can then provide assistance using a remote desktop feature that is included with [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

- **Software license** management.  Track how many software licenses are available, and how many available licenses are being used.

For a complete list of computer management capabilities, see [Windows PC management capabilities in Microsoft Intune](../Topic/Windows_PC_management_capabilities_in_Microsoft_Intune.md).

## <a name="WIT_Adm"></a>Intune administration
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] has a wide array of administrative workspaces that provide you with capabilities that you can use to manage mobile devices and computers. The walkthrough guide will introduce you to the basics. For more details see [Reference for the Microsoft Intune administrative consoles](../Topic/Reference_for_the_Microsoft_Intune_administrative_consoles.md).

|Feature <br /> <br />|Capabilities <br /> <br />|
|-----------|----------------|
|**Account Portal** <br /> <br />|The [Intune account portal](http://go.microsoft.com/fwlink/?LinkID=232813) lets you manage your [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] subscription and specify the users who can access [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. From the [!INCLUDE[wit_icp_2](../Token/wit_icp_2_md.md)], you can manage the service and users by adding user accounts and security groups, setting up and managing service settings, and checking the status of the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] service. You can also contact Microsoft Support and get help from the Microsoft online community. Users can access the [!INCLUDE[wit_icp_2](../Token/wit_icp_2_md.md)] to change their password. <br /> <br />For more information about the [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)], see the [Azure Active Directory Help](http://go.microsoft.com/fwlink/?LinkID=248116). The Azure Active Directory Help provides guidance for Microsoft Online Services such as [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] and Microsoft Office 365, and covers: . <br /> <br /><ul><li>Signing up for a Microsoft Online Service </li><li>Administering your account </li><li>Signing in </li><li>Assigning administrator roles for Microsoft Online Services </li><li>Changing users’ passwords </li> </ul>|
|**Administrator Console:** <br />**Overview workspace** <br /> <br />|Lets you quickly assess the health of the managed devices across your organization. Top tasks include: <br /> <br /><ul><li>view a summary of top alert types </li><li>check the system status of several key areas </li><li>view summaries of the devices that you are managing </li><li>eate a new device or user group </li><li>view a report </li> </ul>If an issue occurs, links appear in the affected area to take you directly to the appropriate workspace to investigate and resolve the problem. <br /> <br />|
|**Administrator Console:** <br />**All Users** <br />and <br />**All Devices** <br />**workspaces** <br /> <br />|These workspaces let you manage your devices and users by organizing them into groups. You can organize groups in the way that best suits your organizational needs (for example, by geographic location, by department, or by hardware characteristics). A device or a user can belong to more than one group. <br /> <br />|
|**Administrator Console:** <br /> **Updates workspace** <br /> <br />|Manage the software update process efficiently for all of the managed devices in your organization. Top tasks include: <br /> <br /><ul><li>View pending updates </li><li>Approve or decline updates </li><li>Configure automatic approval settings for updates </li><li>Set a deadline for update installation </li> </ul>|
|**Administrator Console:** <br />**Protection workspace** <br /> <br />|Helps you enhance the security of all managed computers in your organization by <br /> <br /><ul><li>providing real-time protection against potential threats </li><li>keeping malicious software definitions up to date </li><li>automatically running scheduled scans </li> </ul>This workspace provides Endpoint Protection status summaries, so that if malicious software is detected on a managed computer, or if a computer is not protected, you can quickly identify the affected computers and take appropriate action. <br /> <br />|
|**Administrator Console:** <br /> **Alerts workspace** <br /> <br />|Quickly assess the overall health of managed computers in your organization. Respond to problems so that you can prevent or minimize negative effects on business operations. For example, you can: <br /> <br /><ul><li>View all recent alerts to get an overview of the health of all your managed devices </li><li>Investigate specific issues that are occurring on members of specific groups of managed devices (or, in specific workspaces, such as the **Endpoint Protection** workspace) </li><li>Use filters to see all alerts with a specific severity level, or to review the list of active or closed alerts </li><li>Notify the appropriate people about alerts, using Alert Notification Rules to have [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] send email notifications about specific types of alerts to the right people </li> </ul>|
|**Administrator Console:** <br /> **Software workspace** <br /> <br />|Detect and manage software for all managed devices. In this workspace, you can: <br /> <br /><ul><li>Get an inventory of all software installed on computers (not available for mobile devices) </li><li>Distribute software to computers, including the option to make software required for installation on computers (and install that software without end-user intervention) </li><li>Deploy managed software packages </li><li>Link to a web-based application or an application in the Windows Store for the Windows, Windows RT, Windows Phone 8 and Windows Phone 8.1 platforms; link to an application in the ITunes Store for iOS, or link to an application in Google Play for the Android platform </li><li>Search, sort and filter the lists of managed software or detected software </li> </ul>|
|**Administrator Console:** <br /> **Licenses workspace** <br /> <br />|Add and manage license agreement information for software purchased through Microsoft Volume Licensing agreements, and for Microsoft or non-Microsoft software that was purchased by other means. In this workspace you can: <br /> <br /><ul><li>Enter and manage licenses </li><li>Compare the set of Microsoft licenses in the workspace to the inventory of software detected on your managed computers </li><li>Create license reports to track software installation and license counts </li> </ul>|
|**Administrator Console:** <br /> **Policy workspace** <br /> <br />|Provide settings that control software updates, Endpoint Protection, Windows Firewall settings, and security settings on mobile devices. <br /> <br />|
|**Administrator Console:** <br /> **Reports workspace** <br /> <br />|Run reports that provide information about the software, and hardware and software licenses in your organization. <br /> <br />|
|**Administrator Console:** <br /> **Administration workspace** <br /> <br />|View details about your [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] account (such as account name, status, and active seat count). In this workspace you can manage the following: <br /> <br /><ul><li>**Updates.** Select the products for which you want to manage updates, and determine the types of updates that you want to manage. </li><li>**Alerts and notifications.** Enable alert types that are important, disable those that are not important, set alert thresholds for alert types to notify you if a threshold was met or exceeded, and notify you and other users of alerts using e-mail. </li><li>**Administrator Management.** Designate **Service Administrators** who have permissions to view or edit settings in the Administrator Console; and also assign **Tenant Administrators** who have the same permissions as Service Administrators, and who can also manage administrator accounts using the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Account Portal. </li><li>**Client software download.** Deploy the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] client software manually or automatically. </li><li>**Storage use.** Manage your use of [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Cloud Storage, which is used to distribute software to computers. </li><li>**Mobile device management.** Configure [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] to directly manage mobile devices in your organization </li><li>**Company portal.** Configure the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] company portal to display your company specific information, such as your company name, contact information for IT support, and URLs for your company privacy statement and internal support website. </li> </ul>|

## <a name="WIT_Fre"></a>Intune free trial and pricing
You can start using [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] with a 30-day free trial that includes 100 user licenses. With each user able to use up to 5 devices, you can really get an idea what is possible with [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. To start your free trial, [visit the Intune Sign up page](http://aka.ms/TryMSIntune).

> [!NOTE]
> If your organization has a Microsoft Online Services work or school account, and you might continue with this [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] subscription in production after the trial period ends, click the **Sign in** option on that page and authenticate by using the Global Administrator account for your organization. This action will ensure that your [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] trial links to your existing work or school account. If your organization has an Enterprise Agreement or equivalent volume licensing agreement, please contact your Microsoft representative to set up your free trial.

To learn about [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] pricing, go to the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)][Buy page](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/buy.aspx), and then click **View pricing for [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**.

For step-by-step instructions for free trial signup, and for a walkthrough that you can use to evaluate [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] during your 30-day free trial period, see [Get started with a 30-day trial of Microsoft Intune](../Topic/Get_started_with_a_30-day_trial_of_Microsoft_Intune.md). To purchase a paid subscription, see [Move from a Microsoft Intune free trial to a paid subscription](../Topic/Move_from_a_Microsoft_Intune_free_trial_to_a_paid_subscription.md).

