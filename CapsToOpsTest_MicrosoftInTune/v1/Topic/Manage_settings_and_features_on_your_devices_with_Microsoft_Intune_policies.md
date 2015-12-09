---
description: na
search: na
title: Manage settings and features on your devices with Microsoft Intune policies
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-23
ms.author: dbdc710f437843008017318979c6adba
---
# Manage settings and features on your devices with Microsoft Intune policies
[!INC[wit_firstref](../Token/wit_firstref_md.md)] uses **policies** that help you to configure many security and functional settings for enrolled mobile devices, including:

- Hardware settings, like allowing use of the devices camera, or Bluetooth capability

- Password settings including password length and quality

- Allowed and blocked apps let you configure apps that are compliant, or noncompliant in your organization, and then report on devices that are not compliant (for Windows Phone devices, you can block apps from being installed, or used.

- Kiosk mode settings that allow you to ‘lock down’ certain features of the device like allowing only one app to run, or disabling the power button and volume controls.

Use the information in this topic to help you decide which policy you need to use to manage your devices.

> [!TIP]
> For more detailed information about how to use policies, see [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

## <a name="BKMK_WhatPol"></a>Choose which policy to use

### Android

|Policy name <br /> <br />|Use when you want to <br /> <br />|
|---------------|------------------------|
|**Custom Configuration (Android 4 and later, Samsung KNOX Standard 4.0 and later)** <br /> <br />|<ul><li>Deploy OMA-URI settings, such as Wi-Fi settings that can be used to control device features. This is useful when the setting you need is not available in a configuration policy. </li> </ul>For details, see [Android custom policy settings in Microsoft Intune](../Topic/Android_custom_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**Email Profile (Samsung KNOX Standard 4.0 and later)** <br /> <br />|<ul><li>Create, deploy and monitor Exchange ActiveSync email settings on managed devices. This lets users access corporate email on their personal devices without any required setup on their part. </li> </ul>For details, see [Configure access to corporate email using email profiles with Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**General Configuration (Android 4 and later, Samsung KNOX Standard 4.0 and later)** <br /> <br />|<ul><li>Configure mobile device security and functional settings. </li><li>Specify apps that are compliant or noncompliant, and report when they are used. </li><li>Configure kiosk mode that locks devices to allow only certain features to work, for example, allow the device to run only one app, or disable the volume buttons. </li> </ul>For details, see [Android configuration policy settings in Microsoft Intune](../Topic/Android_configuration_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**PKCS #12 (.PFX) Certificate Profile (Android 4 and later)** <br /> <br />|<ul><li>Use this profile to create and deploy PFX settings for device certificate requests. </li> </ul>For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**SCEP Certificate Profile (Android 4 and later)** <br /> <br />|<ul><li>Configure a Simple Certificate Enrollment Protocol certificate which can be used with a trusted mobile device certificate to authenticate mobile devices to allow them to access network resources such as those configured by Wi-Fi and VPN profiles. </li> </ul>For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**Trusted Certificate Profile (Android 4 and later)** <br /> <br />|<ul><li>Configure a trusted mobile device certificate which can be used to authenticate mobile devices to allow them to access network resources such as those configured by Wi-Fi and VPN profiles. </li> </ul>For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**VPN Profile (Android 4 and later)** <br /> <br />|<ul><li>Configure and deploy settings that give users secure access to your company network from their mobile device. By deploying these settings, you minimize the end-user effort required to connect to their work. </li> </ul>For details, see [Help users connect to their work using VPN profiles with Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**Wi-Fi Profile (Android 4 and later)** <br /> <br />|<ul><li>Configure and deploy wireless network settings to users in your organization. By deploying these settings, you minimize the end-user effort required to connect to the wireless network. </li> </ul>For details, see [Help users connect to company networks using Wi-Fi profiles with Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md). <br /> <br />|

### iOS

|Policy name <br /> <br />|Use when you want to <br /> <br />|
|---------------|------------------------|
|**Custom Configuration (iOS 7.1 and later)** <br /> <br />|<ul><li>Deploy configuration profiles to iOS devices that you created using the Apple Configurator tool. This is useful when the setting you need is not available in a configuration policy. </li> </ul>For details, see [iOS custom policy settings in Microsoft Intune](../Topic/iOS_custom_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**Email Profile (iOS 7.1 and later)** <br /> <br />|<ul><li>Create, deploy and monitor Exchange ActiveSync email settings on managed devices. This lets users access corporate email on their personal devices without any required setup on their part. </li> </ul>For details, see [Configure access to corporate email using email profiles with Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**General Configuration (iOS 7.1 and later)** <br /> <br />|<ul><li>Configure mobile device security and functional settings. </li><li>Specify apps that are compliant or noncompliant, and report when they are used. </li><li>Configure kiosk mode that locks devices to allow only certain features to work, for example, allow the device to run only one app, or disable the volume buttons. </li> </ul>For details, see [iOS configuration policy settings in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**SCEP Certificate Profile (iOS 7.1 and later)** <br /> <br />|<ul><li>Configure a Simple Certificate Enrollment Protocol certificate which can be used with a trusted mobile device certificate to authenticate mobile devices to allow them to access network resources such as those configured by Wi-Fi and VPN profiles. </li> </ul>For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**Trusted Certificate Profile (iOS 7.1 and later)** <br /> <br />|<ul><li>Configure a trusted mobile device certificate which can be used to authenticate mobile devices to allow them to access network resources such as those configured by Wi-Fi and VPN profiles. </li> </ul>For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**VPN Profile (iOS 7.1 and later)** <br /> <br />|<ul><li>Configure and deploy settings that give users secure access to your company network from their mobile device. By deploying these settings, you minimize the end-user effort required to connect to their work. </li> </ul>For details, see [Help users connect to their work using VPN profiles with Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**Wi-Fi Profile (iOS 7.1 and later)** <br /> <br />|<ul><li>Configure and deploy wireless network settings to users in your organization. By deploying these settings, you minimize the end-user effort required to connect to the wireless network. </li> </ul>For details, see [Help users connect to company networks using Wi-Fi profiles with Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**Mobile App Configuration Policy (iOS 7.1 and later)** <br /> <br />|<ul><li>Use mobile app configuration policies to automatically supply settings that might be required when the user runs an iOS app. </li> </ul>For details, see [Configure apps with mobile app configuration policies in Microsoft Intune](../Topic/Configure_apps_with_mobile_app_configuration_policies_in_Microsoft_Intune.md). <br /> <br />|

### Mac OS X

|Policy name <br /> <br />|Use when you want to <br /> <br />|
|---------------|------------------------|
|**Custom Configuration (Mac OS X 10.9 and later)** <br /> <br />|<ul><li>Deploy configuration profiles to Mac computers that you created using the Apple Configurator tool. This is useful when the setting you need is not available in a configuration policy. </li> </ul>For details, see [Mac OS X custom policy settings in Microsoft Intune](../Topic/Mac_OS_X_custom_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**General Configuration (Mac OS X 10.9 and later)** <br /> <br />|<ul><li>Configure mobile device security and functional settings. </li><li>Specify apps that are compliant or noncompliant, and report when they are used. </li> </ul>For details, see [Mac OS X configuration policy settings in Microsoft Intune](../Topic/Mac_OS_X_configuration_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**SCEP Certificate Profile  (Mac OS X 10.9 and later)** <br /> <br />|<ul><li>Configure a Simple Certificate Enrollment Protocol certificate which can be used with a trusted mobile device certificate to authenticate mobile devices to allow them to access network resources such as those configured by Wi-Fi and VPN profiles. </li> </ul>For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**Trusted Certificate Profile (Mac OS X 10.9 and later)** <br /> <br />|<ul><li>Configure a trusted mobile device certificate which can be used to authenticate mobile devices to allow them to access network resources such as those configured by Wi-Fi and VPN profiles. </li> </ul>For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**VPN Profile  (Mac OS X 10.9 and later)** <br /> <br />|<ul><li>Configure and deploy settings that give users secure access to your company network from their mobile device. By deploying these settings, you minimize the end-user effort required to connect to their work. </li> </ul>For details, see [Help users connect to their work using VPN profiles with Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**Wi-Fi Profile (Mac OS X 10.9 and later)** <br /> <br />|<ul><li>Configure and deploy wireless network settings to users in your organization. By deploying these settings, you minimize the end-user effort required to connect to the wireless network. </li> </ul>For details, see [Help users connect to company networks using Wi-Fi profiles with Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md). <br /> <br />|

### Windows
Applies to Windows Phone, and enrolled Windows devices only.

|Policy name <br /> <br />|Use when you want to <br /> <br />|
|---------------|------------------------|
|**Custom Configuration  (Windows 10 Desktop and Mobile and later)** <br /> <br />|<ul><li>Deploy OMA-URI settings that can be used to control device features. This is useful when the setting you need is not available in a configuration policy. <br /> <br />   For a list of available settings, see [Custom URI settings for Windows 10 devices](../Topic/Custom_URI_settings_for_Windows_10_devices.md). </li> </ul>For details, see [Windows 10 custom policy settings in Microsoft Intune](../Topic/Windows_10_custom_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**Custom Configuration (Windows Phone 8.1 and later)** <br /> <br />|<ul><li>Deploy OMA-URI settings that can be used to control device features. This is useful when the setting you need is not available in a configuration policy. </li> </ul>For details, see [Windows Phone custom policy settings in Microsoft Intune](../Topic/Windows_Phone_custom_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**Email Profile (Windows Phone 8 and later)** <br /> <br />**Email Profile (Windows 10 Desktop and Mobile and later)** <br /> <br />|<ul><li>Create, deploy and monitor Exchange ActiveSync email settings on managed devices. This lets users access corporate email on their personal devices without any required setup on their part. </li> </ul>For details, see [Configure access to corporate email using email profiles with Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**General Configuration (Windows 10 Desktop and Mobile and later)** <br /> <br />|<ul><li>Configure mobile device security and functional settings for enrolled Windows 10 desktop and Mobile devices. </li> </ul>For details, see [Windows 10 configuration policy settings in Microsoft Intune](../Topic/Windows_10_configuration_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**General Configuration (Windows 10 Team and later)** <br /> <br />|<ul><li>Configure device security and functional settings for enrolled Windows 10 Team devices (for example, a Surface Hub device). </li> </ul>For details, see [Windows Team configuration policy settings in Microsoft Intune](../Topic/Windows_Team_configuration_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**General Configuration (Windows 8.1 and later)** <br /> <br />|<ul><li>Configure mobile device security and functional settings for enrolled Windows devices. </li> </ul>For details, see [Windows configuration policy settings in Microsoft Intune](../Topic/Windows_configuration_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**General Configuration (Windows Phone 8.1 and later)** <br /> <br />|<ul><li>Configure mobile device security and functional settings. </li><li>Specify apps that users can, or cannot use and block noncompliant apps from being installed or used. </li> </ul>For details, see [Windows Phone configuration policy settings in Microsoft Intune](../Topic/Windows_Phone_configuration_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**PKCS #12 (.PFX) Certificate Profile (Windows 10 Desktop and Mobile and later)** <br /> <br />|<ul><li>Use this profile to create and deploy PFX settings for device certificate requests. </li> </ul>For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**SCEP Certificate Profile (Windows 8.1 and later)** <br /> <br />**SCEP Certificate Profile (Windows Phone 8.1 and later)** <br /> <br />|<ul><li>Configure a Simple Certificate Enrollment Protocol certificate which can be used with a trusted mobile device certificate to authenticate mobile devices to allow them to access network resources such as those configured by Wi-Fi and VPN profiles. </li> </ul>For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**Trusted Certificate Profile (Windows 8.1 and later)** <br /> <br />**Trusted Certificate Profile (Windows Phone 8.1 and later)** <br /> <br />|<ul><li>Configure a trusted mobile device certificate which can be used to authenticate mobile devices to allow them to access network resources such as those configured by Wi-Fi and VPN profiles. </li> </ul>For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**VPN Profile (Windows 10 Desktop and Mobile and later)** <br /> <br />**VPN Profile (Windows 8.1 and later)** <br /> <br />**VPN Profile (Windows Phone 8.1 and later)** <br /> <br />|<ul><li>Configure and deploy settings that give users secure access to your company network from their mobile device. By deploying these settings, you minimize the end-user effort required to connect to their work. </li> </ul>For details, see [Help users connect to their work using VPN profiles with Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md). <br /> <br />|
|**Wi-Fi Import** <br /> <br />|<ul><li>Import and deploy Windows Wi-Fi configurations that you have previously exported to a file. </li> </ul>For details, see [Help users connect to company networks using Wi-Fi profiles with Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md). <br /> <br />|

### Software

|Policy name <br /> <br />|Use when you want to <br /> <br />|
|---------------|------------------------|
|**Managed Browser Policy (Android 4 and later)** <br /> <br />**Managed Browser Policy (iOS 7.1 and later)** <br /> <br />|<ul><li>Specify the websites that users can, and cannot access when they are using the managed browser app. </li> </ul>For details, see [Manage Internet access using managed browser policies with Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md). <br /> <br />|
|**Mobile Application Management Policy (Android 4 and later)** <br /> <br />**Mobile Application Management Policy (iOS 7.1 and later)** <br /> <br />|<ul><li>Modify the functionality of apps that you deploy to help bring them into line with your company compliance and security policies. For example, you can restrict cut, copy and paste operations within a restricted app, or configure an app to open all web links inside the managed browser. </li> </ul>For details, see [Configure and deploy mobile application management policies in the Microsoft Intune console](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md) <br /> <br />|

### Common Mobile Device Settings

|Policy name <br /> <br />|Use when you want to <br /> <br />|
|---------------|------------------------|
|**Exchange ActiveSync Policy** <br /> <br />|<ul><li>Configure mobile device security and functional settings for devices that are managed by Exchange ActiveSync. </li> </ul>For details, see [Exchange ActiveSync policy settings in Microsoft Intune](../Topic/Exchange_ActiveSync_policy_settings_in_Microsoft_Intune.md). <br /> <br />|
|**Mobile Device Security Policy** <br /> <br />|<ul><li>Configures settings for mobile devices (all platforms) including: <br /> <br /><ul><li>Security </li><li>Encryption </li><li>System </li><li>Email </li><li>Applications </li> </ul> </li> </ul> **Important:** [!INC[wit_firstref](../Token/wit_firstref_md.md)] now features separate **configuration policies** for each device platform, and these policies contain the most up-to-date settings you can use. You can continue to use the mobile device security policy and any existing deployments will still work, but you should plan to migrate to the new configuration policies as soon as possible. <br />For details, see [Mobile device security policy settings in Microsoft Intune](../Topic/Mobile_device_security_policy_settings_in_Microsoft_Intune.md). <br /> <br />|

### Conditional access and compliance policies

#### Conditional Access

|Policy name <br /> <br />|Use when you want to <br /> <br />|
|---------------|------------------------|
|**Exchange Online Policy** <br /> <br />**Exchange On-premises Policy** <br /> <br />|<ul><li>Manage access to Microsoft Exchange email from devices that are not managed by [!INC[wit_nextref](../Token/wit_nextref_md.md)] or not compliant with a compliance policy you created. </li> </ul>For details, see [Manage email access with Microsoft Intune](../Topic/Manage_email_access_with_Microsoft_Intune.md). <br /> <br />|
|**SharePoint Online Policy** <br /> <br />|<ul><li>Manage access to SharePoint Online from devices that are not managed by [!INC[wit_nextref](../Token/wit_nextref_md.md)] or not compliant with a compliance policy you created. </li> </ul>For details, see [Manage SharePoint Online access with Microsoft Intune](../Topic/Manage_SharePoint_Online_access_with_Microsoft_Intune.md). <br /> <br />|
> [!NOTE]
> You do not deploy conditional access policies to users and devices. Instead, you configure the required policy and it applies to all groups targeted in the policy.

#### Compliance Policies

|Policy name <br /> <br />|Use when you want to <br /> <br />|
|---------------|------------------------|
|**Compliance policies** <br /> <br />|<ul><li>Define the level of compliance for devices and then report about devices that are noncompliant. These policies are used with conditional access to help evaluate devices that should be blocked from services. </li> </ul>For details, see [Manage device compliance policies for Microsoft Intune](../Topic/Manage_device_compliance_policies_for_Microsoft_Intune.md). <br /> <br />|

### Computer Management

|Policy name <br /> <br />|Use when you want to <br /> <br />|
|---------------|------------------------|
|**Microsoft Intune Agent Settings** <br /> <br />|Configure the [!INC[wit_firstref](../Token/wit_firstref_md.md)] client on computers, including settings for: <br /> <br /><ul><li>Endpoint Protection </li><li>Software updates </li><li>Policy check schedule </li> </ul>This type of policy can be deployed only to groups of devices. <br /> <br />[!INC[wit_nextref](../Token/wit_nextref_md.md)] clients download new and updated policy according to the **Update and application detection frequency** setting, which defaults to 8 hours. However, you can force a refresh of policy on computers at any time. <br /> <br />For details, see [Keep Windows PCs up to date with software updates in Microsoft Intune](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md). <br /> <br />|
|**Microsoft Intune Center Settings** <br /> <br />|Configure details that appear in the [!INC[wit_firstref](../Token/wit_firstref_md.md)] Center on managed computers. <br /> <br />This type of policy can be deployed only to groups of devices. <br /> <br />For details, see [Common Windows PC management tasks with the Microsoft Intune computer client](../Topic/Common_Windows_PC_management_tasks_with_the_Microsoft_Intune_computer_client.md). <br /> <br />|
|**Windows Firewall Settings** <br /> <br />|Configures Windows Firewall settings and exceptions for common network communications on computers, including: <br /> <br /><ul><li>BranchCache </li><li>Remote Assistance </li><li>Media sharing </li> </ul>This type of policy can be deployed only to groups of devices. <br /> <br />For details, see [Help secure Windows PCs with Endpoint Protection for Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md). <br /> <br />|

## See Also
[Configure and manage devices with Microsoft Intune](../Topic/Configure_and_manage_devices_with_Microsoft_Intune.md)
[Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

