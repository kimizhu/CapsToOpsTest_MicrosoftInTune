---
description: na
search: na
title: Mobile%20device%20management%20capabilities%20in%20Microsoft%20Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-18
ms.author: f93f38ed286b4cbb94b9b427a0abc63e
---
# Mobile%20device%20management%20capabilities%20in%20Microsoft%20Intune
Intune supports mobile device management of iOS, Android, and Windows Phone devices. It also supports management of Windows RT, Window computers, and Mac OS X computers as mobile devices. Users use a *company portal* to install apps, enroll and remove devices, and helps them contact their IT department or helpdesk. To enroll mobile devices you must set [!INC[wit_nextref](../Token/wit_nextref_md.md)] as your *mobile device authority* and then configure the infrastructure to support the platforms you want to managed. This requires establishing a trust relationship with the device.

## <a name="BKMK_MobileDeviceReqs"></a>Supported mobile devices
The requirements to manage a mobile device and the level of management you have depend on whether you manage the device directly or use Exchange ActiveSync:

- **Direct management**: Different types of mobile devices have different requirements for direct management. For example, to manage iOS devices you need an Apple Push Notification service certificate, and to manage apps for a [!INC[winblue_winrt_2](../Token/winblue_winrt_2_md.md)] device, you need sideloading keys and a code-signing certificate. [!INC[wit_nextref](../Token/wit_nextref_md.md)] can manage the following devices with mobile device management:

   - Apple iOS 7.1 and later

      > [!NOTE]
      > iOS 6.0 devices that are already enrolled will remain enrolled, but new devices must be running iOS version 7.1 or later in order to enroll in Intune.

   - Google Android 4.0 and later (including Samsung KNOX)

   - Windows Phone 8.0 and later

   - Windows RT and Windows 8.1 RT

   - Windows 8.1 and later computers (managed as mobile devices; see [Windows PC management capabilities in Microsoft Intune](../Topic/Windows_PC_management_capabilities_in_Microsoft_Intune.md))

   - Mac OS X 10.9 and later

   Before you can directly manage mobile devices you must [Set mobile device management authority as Microsoft Intune](../Topic/Set_mobile_device_management_authority_as_Microsoft_Intune.md).

- **Exchange ActiveSync**: To manage devices by using Exchange ActiveSync requires you to install the On-Premises Connector or use the built-in Service to Service Connector to connect to your Exchange Server.

   To learn about the hardware and software requirements to install the On-Premises Connector, see [Requirements for the On-Premises Connector](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_ExchanceConnectorReqs).

   To learn about using the On-Premises Connector or Service to Service Connector with Exchange, see [Mobile device management with Exchange ActiveSync and Microsoft Intune](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md).

## Mobile device management features
Intune supports mobile device management of iOS, Android, and Windows Phone devices. It also supports management of Windows RT and Window computers as mobile devices. [!INC[wit_nextref](../Token/wit_nextref_md.md)] can manage users' devices, popularly known as "bring your own device" (BYOD). It can also manage company-owned devices including scenarios where the company provides a list of devices users may choose from, known as "choose your own device" (CYOD).

You can enroll devices to meet your organization's needs:

|Enrollment type <br /> <br />|BYOD <br /> <br />|CYOD <br /> <br />|Shared device with manager account <br /> <br />|Shared device without a user account <br /> <br />|
|-------------------|--------|--------|--------------------------------------|----------------------------------------|
|**Description** <br /> <br />|Personal device enrolled using Microsoft Intune <br /> <br />|Corporate-owned device for single user <br /> <br />|Corporate-owned device managed using a manager account shared by many users <br /> <br />|Corporate-owned user-less device used by many users. <br /> <br />|
|**Device’s user** <br /> <br />|Owner <br /> <br />|Assigned user <br /> <br />|No user-specific account <br /> <br />|No specific user <br /> <br />|
|**Who enrolls** <br /> <br />|Owner <br /> <br />|Administrator <br /> <br />|Device Manager <br /> <br />|Anyone <br /> <br />|
|**Who un-enrolls** <br /> <br />|Owner or administrator <br /> <br />|Administrator <br /> <br />|Administrator <br /> <br />|Administrator <br /> <br />|
|**Who can reset** <br /> <br />|Owner or administrator <br /> <br />|Administrator <br /> <br />|Administrator <br /> <br />|Administrator <br /> <br />|
To enroll mobile devices you must set [!INC[wit_nextref](../Token/wit_nextref_md.md)] as your *mobile device authority* and then configure the infrastructure to support the platforms you want to managed. This requires establishing a trust relationship with the device.

Management, inventory, app deployment, provisioning, and retirement are all handled through the [!INC[wit_nextref](../Token/wit_nextref_md.md)] administration console. Users gain access to the company portal which allows them to install apps, enroll and remove devices, and helps them contact their IT department or helpdesk.

**Mobile device management (MDM) capabilities** differ across mobile device platforms but all platforms support the following:

- **Certificate, email, VPN and Wifi profiles.** You can deploy certificate profiles to mobile devices, and also deploy e-mail, VPN and Wifi profiles. See [Enable access to company resources with Microsoft Intune](http://msdn.microsoft.com/en-us/library/5b090c5a-6f12-4e60-ace0-c9929afaa9a3).

- **Manage corporate-owned iOS devices.** You can set up devices for enrollment and then distribute them to specific users, or you can enroll devices so that they can be shared by multiple users. See [Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).

- **Mobile application management.** Managed mobile apps can be configured to restrict certain app operations, such as copy and paste, to help protect your organization’s data. You can also use the managed browser to control the sites that users are allowed to visit. See [Configure and deploy mobile application management policies in the Microsoft Intune console](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md) and [Manage Internet access using managed browser policies with Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md).

- **Conditional access.** Use [!INC[wit_nextref](../Token/wit_nextref_md.md)] conditional access policies to control access to on-premises Microsoft Exchange email from mobile devices, even when the device is not managed by Intune. See [Manage access to email and SharePoint with Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md).

- **Passwords management** differs across mobile device platforms, but all platforms let you require a password, limit the number of failed attempts, limit the minutes before the screen locks, set password expiration, and prevent previously-used passwords.

- **Application settings.** You can control browser settings, and also such application settings as whether app stores can be used on mobile devices.

- **Device capabilities, cellular and voice.** You can allow or deny the use of a camera, control roaming settings, and enable or disable iOS voice assistant and voice dialing features.

- **Reset passcodes, lock, selectively wipe or retire devices.** You can reset passcodes if users lose access to their device, lock missing or stolen devices, or even wipe data off of missing or stolen devices.

## Device security and configuration

|Capability <br /> <br />|Details <br /> <br />|More information <br /> <br />|
|--------------|-----------|--------------------|
|Configuration policies <br /> <br />|Mobile device configuration policies let you manage many settings and features on mobile devices in your organization. <br /> <br />|[iOS configuration policy settings in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Android configuration policy settings in Microsoft Intune](../Topic/Android_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Windows configuration policy settings in Microsoft Intune](../Topic/Windows_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Windows Phone configuration policy settings in Microsoft Intune](../Topic/Windows_Phone_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Exchange ActiveSync policy settings in Microsoft Intune](../Topic/Exchange_ActiveSync_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Mobile device security policy settings in Microsoft Intune](../Topic/Mobile_device_security_policy_settings_in_Microsoft_Intune.md) <br /> <br />|
|Custom policies <br /> <br />|Use custom polices when configuration policies do not contain the setting you require. For iOS devices, you can import settings you exported from the Apple Configurator Tool. For other devices, you can use OMA-URI settings to configure settings and features on the device. <br /> <br />|[iOS custom policy settings in Microsoft Intune](../Topic/iOS_custom_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Android custom policy settings in Microsoft Intune](../Topic/Android_custom_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Windows Phone custom policy settings in Microsoft Intune](../Topic/Windows_Phone_custom_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Windows 10 custom policy settings in Microsoft Intune](../Topic/Windows_10_custom_policy_settings_in_Microsoft_Intune.md) <br /> <br />|
|Remote Wipe, Remote Lock, and Passcode Reset <br /> <br />|Erase sensitive data when a device is lost or stolen. For example, you can remotely lock the device, restore it to factory settings, or wipe only corporate data. <br /> <br />|[Help protect your data with remote wipe, remote lock, or passcode reset using Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md) <br /> <br />|
|Kiosk mode <br /> <br />|Lets you lock down certain features of mobile devices such as screen capture and the power switch. Also lets you restrict devices to run a single app that you specify. <br /> <br />|[iOS configuration policy settings in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />|

## App management

|Capability <br /> <br />|Details <br /> <br />|More information <br /> <br />|
|--------------|-----------|--------------------|
|App deployment and management <br /> <br />|Provides a range of tools to help you manage mobile apps through their lifecycle, including app deployment from installation files and app stores, detailed monitoring of app status, and app removal. <br /> <br />|[Deploy apps to mobile devices in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune.md) <br /> <br />|
|Compliant and noncompliant apps <br /> <br />|Lets you specify lists of compliant apps (that users are allowed to install) and noncompliant apps (which must not be installed by users). <br /> <br />|[iOS configuration policy settings in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />|
|Mobile application management <br /> <br />|Configure restrictions for apps by using a mobile application management policy. This helps you to increase the security of your company data by restricting operations such as copy and paste, external backup of data and the transfer of data between apps. <br /> <br />|[Configure and deploy mobile application management policies in the Microsoft Intune console](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md) <br /> <br />[Prepare iOS apps for mobile application management with the Microsoft Intune App Wrapping Tool](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md) <br /> <br />[Prepare Android apps for mobile application management with the Microsoft Intune App Wrapping Tool](../Topic/Prepare_Android_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md) <br /> <br />[Microsoft apps you can use with Microsoft Intune mobile application management policies](../Topic/Microsoft_apps_you_can_use_with_Microsoft_Intune_mobile_application_management_policies.md) <br /> <br />|
|Managed browser <br /> <br />|After you deploy the managed browser to your users, you can configure a managed browser policy to control the websites that they can visit. In addition, you can also apply mobile application management policies to the managed browser. <br /> <br />|[Manage Internet access using managed browser policies with Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md) <br /> <br />|

## Company resource access

|Capability <br /> <br />|Details <br /> <br />|More information <br /> <br />|
|--------------|-----------|--------------------|
|Certificate profiles <br /> <br />|Create and deploy trusted certificate profiles and Simple Certificate Enrollment Protocol (SCEP) certificates which can be used to help secure and authenticate Wi-Fi, VPN, and email profiles. <br /> <br />|[Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md) <br /> <br />|
|Wi-Fi profiles <br /> <br />|Deploy wireless network settings to your users. By deploying these settings, you minimize the end-user effort required to connect to the corporate network. <br /> <br />|[Help users connect to company networks using Wi-Fi profiles with Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md) <br /> <br />|
|Email profiles <br /> <br />|Create and deploy email settings to devices. This lets users access corporate email on their personal devices without any required setup on their part. <br /> <br />|[Configure access to corporate email using email profiles with Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md) <br /> <br />|
|VPN profiles <br /> <br />|Deploy VPN settings to users and devices in your organization. By deploying these settings, you minimize the end-user effort required to connect to resources on the company network. <br /> <br />|[Help users connect to their work using VPN profiles with Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md) <br /> <br />|
|Conditional access policies <br /> <br />|Manage access to Microsoft Exchange email and SharePoint Online from devices that are not managed by [!INC[wit_nextref](../Token/wit_nextref_md.md)]. <br /> <br />|[Manage access to email and SharePoint with Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md) <br /> <br />|

## Inventory and reporting

|Capability <br /> <br />|Details <br /> <br />|More information <br /> <br />|
|--------------|-----------|--------------------|
|Inventory and reporting <br /> <br />|Find information about the devices you manage and the software they are using. <br /> <br />You can filter these reports in a number of ways, such as the device platform, and whether the device is compliant with corporate standards. <br /> <br />|[Understand Microsoft Intune operations by using reports](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md) <br /> <br />|

## See Also
[Introduction to Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)
[Get ready to enroll devices in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)
[Manage mobile devices and PCs from the cloud](http://technet.microsoft.com/library/dn715906.aspx)
[Bring your own device (BYOD) design considerations guide](http://technet.microsoft.com/library/dn656905.aspx)
[Sign up for a free trial](https://account.manage.microsoft.com/Signup/MainSignUp.aspx?OfferId=A77BE827-FC8B-4EF2-A0F5-7CD6C813AA65&amp;ali=1)
[How to buy Intune](http://technet.microsoft.com/library/dn646949.aspx)
[Start using Microsoft Intune](../Topic/Start_using_Microsoft_Intune.md)
[Microsoft Intune Service Description](../Topic/Microsoft_Intune_Service_Description.md)
[Get started with a 30-day trial of Microsoft Intune](../Topic/Get_started_with_a_30-day_trial_of_Microsoft_Intune.md)

