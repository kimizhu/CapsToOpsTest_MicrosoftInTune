---
description: na
keywords: na
pagetitle: What&#39;s new in Microsoft Intune
search: na
ms.date: 2015-12-02
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: fab51ee0-638d-4dd4-8d8f-1f263bc11e5c
ms.author: d4484712-0a03-4345-bdeb-64372a73012b
---
# What&#39;s new in Microsoft Intune

## What’s new in Intune -- November 2015

### App management
Intune supports mobile application management (MAM) policies that help prevent corporate data from being leaked to consumer apps or services. Historically, these policies would only be enforced on mobile apps running on devices that were also enrolled for mobile device management (MDM) into Intune.

With this month's update, Intune is expanding its MAM capabilities to new classes of devices. In addition to devices enrolled into Intune, you can now enforce MAM policies on:

- devices managed by any other device management (MDM) solution

- devices that are not enrolled into any device management system, typically bring-your-own (BYO) devices

You can find more information about these new MAM capabilities in the following blog posts:

- [Enhancing managed mobile productivity](http://blogs.technet.com/b/microsoftintune/archive/2015/11/17/enhancing-managed-mobile-productivity.aspx)

- [Announcing new Microsoft Enterprise Mobility capabilities](http://blogs.technet.com/b/microsoftintune/archive/2015/11/17/enhancing-managed-mobile-productivity.aspx)

Additionally, here are some highlights and additional information about Intune's MAM features:

- Corporate data is isolated from consumer data within apps enlightened for Intune including Office Mobile apps, third-party apps that have adopted the Intune SDK, or line-of-business apps wrapped by Intune.

- Company data can be shared (**cut/copy/paste**) across company apps, while preventing the sharing of company data into personal apps. Read [How MAM policies protect app data](../Topic/Configure_data_loss_prevention_app_policies_with_Microsoft_Intune.md#bkmk_howMAMworks) for more details. This example scenario, [Scenario: Microsoft Word app for work and personal tasks](../Topic/End-user_experience_for_apps_associated_with_Microsoft_Intune_mobile_app_management_policies.md#bkmk_wordworkandpersonal), shows how sharing company data into personal apps is prevented.

- Key data loss prevention policies like: per-App PIN, save-as controls,  and managed data sharing between apps. Read [Create and deploy mobile app management policies with Microsoft Intune](../Topic/Create_and_deploy_mobile_app_management_policies_with_Microsoft_Intune.md)to see a list of all the policies.

- Word, Excel, PowerPoint, Outlook, OneNote,  and OneDrive for Business all have these new capabilities and can be managed with and without device enrollment.   The data loss protection capabilities are natively built into the standard Office apps in the Apple Store or the Google Play store, and do not require app wrapping or sideloading.

- To learn how to get started, see [Get started with mobile app management policies in the Azure portal](../Topic/Get_started_with_mobile_app_management_policies_in_the_Azure_portal.md). To learn how to configure and deploy mobile app management policies, see [Create and deploy mobile app management policies with Microsoft Intune](../Topic/Create_and_deploy_mobile_app_management_policies_with_Microsoft_Intune.md).

- When end-users authenticate to the app with their corporate credentials, the data loss protection capabilities are automatically set up.

   The [End-user experience for apps associated with Microsoft Intune mobile app management policies](../Topic/End-user_experience_for_apps_associated_with_Microsoft_Intune_mobile_app_management_policies.md) topic has some example scenarios for accessing OneDrive on iOS and Android devices.

- Works on both iOS and Android devices.

The list of [Microsoft apps you can use with Microsoft Intune mobile application management policies](https://technet.microsoft.com/library/dn708489.aspx) has been updated to show the latest apps.

### Device management

#### Mac OS X device management
With [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], you can now enroll and manage Mac OS X devices. You can do the following with your Mac OS X devices:

- Enroll devices to be managed by [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. See [Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md)

- Control device settings with a general configuration policy. See [Mac OS X configuration policy settings in Microsoft Intune](../Topic/Mac_OS_X_configuration_policy_settings_in_Microsoft_Intune.md)

- Deploy Mac OS X settings you created with the Apple Configurator. See [Mac OS X custom policy settings in Microsoft Intune](../Topic/Mac_OS_X_custom_policy_settings_in_Microsoft_Intune.md)

- Collect hardware and software inventory from Mac OS X devices. See [Understand your devices with inventory in Microsoft Intune](../Topic/Understand_your_devices_with_inventory_in_Microsoft_Intune.md)

- Run new reports that display details about the Mac OS X devices you manage. See [Understand Microsoft Intune operations by using reports](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md)

#### New Edge browser settings for Windows 10 devices
New settings have been added to the Windows 10 general configuration policy that let you manage settings and features of the Microsoft Edge browser. See [Windows 10 configuration policy settings in Microsoft Intune](../Topic/Windows_10_configuration_policy_settings_in_Microsoft_Intune.md).

#### Email profiles
A new email profiles policy has been added for Windows 10 desktop and Windows 10 mobile devices. See [Manage settings and features on your devices with Microsoft Intune policies](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md).

#### New compliance policy settings
The following new security and system policy settings have been added to the list of compliance policies:

- To make sure that Windows 8.1 or later devices that access your company resources have the latest updates installed, use the  **Require automatic updates** setting. You can also specify the type of updates to be automatically installed -- either all updates marked as important to be installed, or  all updates marked important or recommended. For the full list of compliance policy settings, see [Manage device compliance policies for Microsoft Intune](../Topic/Manage_device_compliance_policies_for_Microsoft_Intune.md).

- The new **Require a password when the device returns from the idle state** setting combined with the existing **Minutes of inactivity before password is required** setting allows you to create a compliance setting that requires the end-user to enter a password to use a device that has been inactive for a certain time.

#### New conditional access policy options
You can apply conditional access policies to **all users** in either new or existing conditional access policies.   All users licensed for Intune and Office 365 will be required to enroll their devices, and if the device platform is not supported by Intune, access is blocked for client applications using [Active Directory authentication based sign-in (modern authentication)](https://blogs.office.com/2014/11/12/office-2013-updated-authentication-enabling-multi-factor-authentication-saml-identity-providers/).

You can also specify that the conditional access policy applies to **all platforms**.  Any client application using the [Active Directory authentication based sign-in (modern authentication)](https://blogs.office.com/2014/11/12/office-2013-updated-authentication-enabling-multi-factor-authentication-saml-identity-providers/) is subject to the conditional access policy, and if the platform is not supported by Intune, it will be blocked.

### Changes and updates to Microsoft Company Portal
The following changes have been made to the company portal apps in this release:

**iOS**

- Intune now supports the enrollment of Mac OS X devices  by using  the [Company Portal website](https://portal.manage.microsoft.com). For instructions, see [Enroll your Mac OS X device in Intune](https://technet.microsoft.com/library/mt598622.aspx).

**Company Portal website**

- Users who have enrolled their device in Intune can now reset their passcode by using the **Reset Passcode** option on the Company Portal website. Previously, only IT administrators could reset users' passcodes. The  Reset Passcode option is not supported on Windows 8.1 and Windows RT devices, and the option appears only when devices are enrolled in mobile device management (MDM) or MDM with Exchange ActiveSync. For user instructions, see [Reset your passcode](https://technet.microsoft.com/library/mt590895.aspx).

## Changes to tenant admin licensing requirement
An Intune subscription (license) is required to enroll devices into Intune for mobile apps to receive MAM policy.

To date, an exception to this license requirement was granted for users with administrative rights to the Intune service.  Starting in January, administrative user accounts will need to have an Intune or EMS license assigned in order to enroll devices or receive MAM policy.  Admin accounts that do not need to enroll devices or receive MAM policy (such as helpdesk staff) will continue to be able to log into the console and perform administrative tasks without a subscription.

## <a name="BKMK_WhatsComing"></a>What’s coming
Keep informed about upcoming developments for Intune with the [Cloud Platform roadmap](http://www.microsoft.com/en-us/server-cloud/roadmap/Indevelopment.aspx?TabIndex=0&amp;dropValue=Intune).

### Protect your company data using enterprise data protection (EDP)
When managing Windows 10 devices, Intune will be able to create and deploy configuration policies for Windows 10 enterprise data protection (EDP). EDP can help you restrict and/or alert you to company data sharing. Intune EDP policies will manage the list of apps protected by EDP, enterprise network locations, protection level, and encryption settings. To opt-in to receive preview builds of Windows, consider joining the [Windows Insider Program](https://insider.windows.com/).

> [!NOTE]
> Enterprise data protection is currently being tested with a number of enterprise customers, and will become available to Windows Insiders soon.

## What's new in Intune documentation
**New content**

|||
|-|-|
|**Title** <br /> <br />|**Details** <br /> <br />|
|[Mac OS X configuration policy settings in Microsoft Intune](../Topic/Mac_OS_X_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />|Contains information about how to control device settings and features for Mac OS X devices. <br /> <br />|
|[Mac OS X custom policy settings in Microsoft Intune](../Topic/Mac_OS_X_custom_policy_settings_in_Microsoft_Intune.md) <br /> <br />|Contains information about how to deploy Mac OS X device settings that you created using the Apple Configurator tool. <br /> <br />|
|[Configure data loss prevention app policies with Microsoft Intune](../Topic/Configure_data_loss_prevention_app_policies_with_Microsoft_Intune.md) <br /> <br />|Contains information about the scenarios that mobile app management policies support and  how the policy works to protect data. <br /> <br />|
|[Get started with mobile app management policies in the Azure portal](../Topic/Get_started_with_mobile_app_management_policies_in_the_Azure_portal.md) <br /> <br />|Contains information about what you need to get started using the Azure preview portal for mobile app management policies. <br /> <br />|
|[Create and deploy mobile app management policies with Microsoft Intune](../Topic/Create_and_deploy_mobile_app_management_policies_with_Microsoft_Intune.md) <br /> <br />|Contains a step by step walkthrough of how to create mobile app management policies in the Azure preview portal <br /> <br />|
|[Monitor mobile app management policies with Microsoft Intune](../Topic/Monitor_mobile_app_management_policies_with_Microsoft_Intune.md) <br /> <br />|Contains information on how you can monitor your mobile app management policies using the Azure preview portal <br /> <br />|
|[Microsoft Intune mobile app management policies and iOS Open In](../Topic/Microsoft_Intune_mobile_app_management_policies_and_iOS_Open_In.md) <br /> <br />|Contains information on how mobile app management policies work with iOS Open In feature <br /> <br />|
|[End-user experience for apps associated with Microsoft Intune mobile app management policies](../Topic/End-user_experience_for_apps_associated_with_Microsoft_Intune_mobile_app_management_policies.md) <br /> <br />|Contains information on what the end-user experience is when using apps associated with mobile app management policy. <br /> <br />|
|[Wipe managed company app data with Microsoft Intune](../Topic/Wipe_managed_company_app_data_with_Microsoft_Intune.md) <br /> <br />|Contains information on how you can remove company app data. <br /> <br />|
**Updated content**

|||
|-|-|
|**Title** <br /> <br />|**Details** <br /> <br />|
|[Windows 10 configuration policy settings in Microsoft Intune](../Topic/Windows_10_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />|Added new Edge browser settings. <br /> <br />|
|[Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) <br /> <br />|Added information about how to enroll Mac OS X devices. <br /> <br />|
|[Understand your devices with inventory in Microsoft Intune](http://msdn.microsoft.com/en-us/library/adb8c9cb-3d7b-4f6c-b77f-592b488c37b2) <br /> <br />|Added information about the inventory collected from Mac OS X devices. Also, updated the topic with the latest information for all device platforms. <br /> <br />|
|[Understand Microsoft Intune operations by using reports](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md) <br /> <br />|Added information about the two new reports used to display information about your managed Mac OS X devices. <br /> <br />|
|[Manage device compliance policies for Microsoft Intune](../Topic/Manage_device_compliance_policies_for_Microsoft_Intune.md) <br /> <br />|Added information about the new compliance policies for requiring automatic updates and password requirement when a device returns from idle state. <br /> <br />|
|[Manage email access with Microsoft Intune](../Topic/Manage_email_access_with_Microsoft_Intune.md) <br /> <br />|Added information about the ability to apply the conditional access  policy to all platforms and all users. <br /> <br />|
|[Manage SharePoint Online access with Microsoft Intune](../Topic/Manage_SharePoint_Online_access_with_Microsoft_Intune.md) <br /> <br />|Added information about the ability to apply conditional access policy to all platforms and all users. <br /> <br />|

## <a name="bkmk_top"></a>Archive

- [October 2015](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_Oct2015)

- [September 2015](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_Sep2015)

- [August 2015](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_August2015)

- [July 2015](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_Jul15)

- [June 2015](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_Jun15)

- [May 2015](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_May15)

- [April 2015](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_Apr15)

- [March 2015](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_Mar15)

- [February 2015](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_Feb15)

- [December 2014](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_Dec14)

- [November 2014](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_Nov14)

- [September 2014](../Topic/What_s_new_in_Microsoft_Intune.md#BKMK_Sep14)

- [April 2014](../Topic/What_s_new_in_Microsoft_Intune.md#bkmk_ape)

- [January 2014](../Topic/What_s_new_in_Microsoft_Intune.md#bkmk_Jan2014)

- [October 2013](../Topic/What_s_new_in_Microsoft_Intune.md#bkmk_Oct2013)

- [June 2013](../Topic/What_s_new_in_Microsoft_Intune.md#bkmk_June2013)

- [May 2013](../Topic/What_s_new_in_Microsoft_Intune.md#bkmk_May2013)

- [April 2013](../Topic/What_s_new_in_Microsoft_Intune.md#bkmk_April2013)

- [March 2013](../Topic/What_s_new_in_Microsoft_Intune.md#bkmk_March2013)

### <a name="BKMK_Oct2015"></a>October 2015

#### Updates to conditional access for Exchange on-premises

- **You can now allow access to Exchange Active Sync email for compliant devices enrolled in Intune when the global Exchange rule is set to block or quarantine**

   Until now, to allow email access on enrolled and compliant devices,  you had to set the default global Exchange rule to **Allow**.

   With this service update, this setting is no longer a requirement for conditional access.  If your Exchange environment requires that your default global rule to be set to **Block/Quarantine**, simply check the **Default Rule Override** checkbox in the Exchange on-premises conditional access policy page.  The [Manage email access with Microsoft Intune](../Topic/Manage_email_access_with_Microsoft_Intune.md) topic has more details on the rules and the resulting end user notifications.

- **New one-click quarantine experience**

   We have simplified the quarantine email experience to allow one-click enrollment. With this service update, end users can click  a single link in the quarantine email to complete the  enrollment process within the company portal app.

#### Mobile device and app management updates

- **Android**

   All [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] management features now support Android 6.0 (Marshmallow) as described in this blog post: [Microsoft Intune Provides Day 0 Support for Android Marshmallow](http://blogs.technet.com/b/microsoftintune/archive/2015/10/09/microsoft-intune-to-provide-day-0-support-for-android-marshmallow.aspx).

- **iOS**

   You can no longer create new app deployments to iOS devices running a version earlier than iOS 7.1. Any existing app deployments to devices running an earlier version than iOS 7.1 will continue to work and be managed by [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

- **Windows 10**

   [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] now supports deploying Windows 10 Universal apps using the **Windows app package** software installer type. For details and requirements, see [Plan for app deployment in Microsoft Intune](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md).

#### Changes and updates to Microsoft Company Portal apps
The following changes have been made to the company portal apps in this release:

**iOS**

- New buttons have been added to the Company Portal app to make it easier for users to send diagnostic logs to their IT admins:

   |Button name <br /> <br />|Where it appears <br /> <br />|
   |---------------|--------------------|
   |**Report** <br /> <br />|Error alert messages <br /> <br />|
   |**Send Diagnostic Report** <br /> <br />|About screen of the Company Portal app <br /> <br />|

### <a name="BKMK_Sep2015"></a>September 2015

#### Mobile device and app management updates

- **All [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] iOS management features now support iOS 9**
   For details about iOS 9 management capabilities, see [this blog post](http://blogs.technet.com/b/microsoftintune/archive/2015/09/09/day-zero-support-for-ios-9-with-intune.aspx).

- **New mobile app configuration policy for iOS**
   Use the new mobile app configuration policy to automatically supply settings that an iOS app might need when it is run. For example, you could supply a network port, or a user name. For details, see [Configure apps with mobile app configuration policies in Microsoft Intune](../Topic/Configure_apps_with_mobile_app_configuration_policies_in_Microsoft_Intune.md).

- **Easier app management for iOS 9 users** 
   In this release, you can bring already-deployed apps under Intune management for iOS 9 users. For earlier versions of iOS, when you deploy an app and an unmanaged version of the app is already installed on a device, you still have to ask the user to uninstall the app manually before [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] can install the managed app.

   But starting with this release of Intune, you   can now prompt users of iOS 9 devices to allow Intune to take over management of the app and apply any relevant mobile application management policies.

- **Windows 10 management**
   Use the new [Windows 10 general configuration policy](https://technet.microsoft.com/library/mt404697.aspx) to configure password, device, browser and other settings for enrolled devices that run Windows 10 and Windows 10 Mobile

- **Create and deploy apps to enrolled Windows 10 devices**
   A new software installer type, Windows Installer through MDM (&#42;.msi) lets you create and deploy Windows Installer apps to enrolled devices that run Windows 10. For details, see [Plan for app deployment in Microsoft Intune](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md).

### Changes and updates to Microsoft Company Portal apps
The following changes have been made to the company portal apps in this release:

**iOS**

- Microsoft automatically collects anonymous data about the performance and use of the company portal to improve Microsoft products and services. End users can turn off data collection by using the Usage Data setting on their device, but administrators have no control over the data collection and cannot change the end user’s selection for this setting.

- Full screen resolution support on iPhone 6 and 6 Plus

- Bug fixes to improve security

### What's new in Intune documentation -- September 2015

#### New topics

|Name <br /> <br />|Details <br /> <br />|
|--------|-----------|
|[Windows 10 configuration policy settings in Microsoft Intune](../Topic/Windows_10_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />|This is a new configuration policy that lets you manage settings and features on devices that run Windows 10 and Windows 10 Mobile. <br /> <br />|
|[Configure apps with mobile app configuration policies in Microsoft Intune](../Topic/Configure_apps_with_mobile_app_configuration_policies_in_Microsoft_Intune.md) <br /> <br />|This is a new policy type that lets you automatically supply settings that might be required when the user runs an iOS app. <br /> <br />|

#### Updated topics

|Name <br /> <br />|Details <br /> <br />|
|--------|-----------|
|[Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md) <br /> <br />|Updated to include the latest information to help you understand and create policies. <br /> <br />|

### <a name="BKMK_August2015"></a>August 2015

#### Mobile device and app management updates

- **Terms and conditions** for Intune enrollment and company access are [now managed using policies](https://technet.microsoft.com/library/mt405893.aspx). You can target different sets of terms and conditions to meet specific user group requirements. For example, you can  deploy terms and conditions in different languages to geographically defined user groups. You can also [edit your terms and conditions](https://technet.microsoft.com/library/mt405893.aspx#BKMK_TCVers) and specify whether to increment the version numbers, requiring users to agree to the new terms and conditions before they can use the company portal.

- **A number of Intune policies have been renamed** to make them more consistent across the product and easier for you to find. For a list of all available Intune policies, see [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

- **PKCS #12 (.PFX) Certificate Profiles** are available for Android 4.0 or later, and Windows 10 (desktop and mobile) and later. Using .PFX does not require an NDES server. Learn how to use .PFX certificate profiles in [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).

- **Corporate Boundaries settings for Windows 10 Desktop and Mobile** enable granular VPN settings, as described in [Help users connect to their work using VPN profiles with Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md).

- **The OneDrive app for Android now supports multi-identity**. This and other updates to mobile app management policies are described in the [list of Microsoft applications you can manage](https://technet.microsoft.com/library/dn708489.aspx).

- **iOS Activation Lock bypass**. If company-owned iOS devices are protected by Activation Lock, you must enter the user's Apple ID and password before you can erase or reactivate the device. This can present a challenge when users leave the company and return a company-owned device without turning off Activation Lock. To help solve this problem, you can use [Intune Activation Lock Bypass](https://technet.microsoft.com/library/mt414176.aspx).

#### Conditional access for PCs
You can now configure conditional access policies for PCs. This allows Office desktop apps to access Exchange Online and SharePoint online services. 
To enable conditional access policy for PCs, the PC must either be domain joined or be complaint.

- See the **Getting started** section in  [Manage access to email and SharePoint with Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md) for the full list of requirements to enable conditional access for PCs.

- See [Manage email access with Microsoft Intune](../Topic/Manage_email_access_with_Microsoft_Intune.md) for options you can set to enable conditional access for email access.

- See [Manage SharePoint Online access with Microsoft Intune](../Topic/Manage_SharePoint_Online_access_with_Microsoft_Intune.md) for options you can set to enable conditional access for SharePoint Online.

#### Changes and updates to Microsoft Company Portal apps
The following changes have been made to the company portal apps in this release:

**Android**

- Users will now see device enrollment instructions after signing in if they have not yet enrolled their device for management.

#### What's new in Intune documentation -- August 2015

##### New topics

|Name <br /> <br />|Details <br /> <br />|
|--------|-----------|
|[Help protect iOS devices with Activation Lock bypass for Microsoft Intune](../Topic/Help_protect_iOS_devices_with_Activation_Lock_bypass_for_Microsoft_Intune.md) <br /> <br />|Learn about how you can use Intune to bypass iOS Activation lock when a user leaves the company and returns a locked device. <br /> <br />|

##### Updated topics

|Name <br /> <br />|Details <br /> <br />|
|--------|-----------|
|[Microsoft apps you can use with Microsoft Intune mobile application management policies](../Topic/Microsoft_apps_you_can_use_with_Microsoft_Intune_mobile_application_management_policies.md) <br /> <br />|Updated with the latest information about apps you can manage with mobile application management policies. <br /> <br />|
|[Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md) <br /> <br />|Updated with the newest policies added to Intune. <br /> <br />|

### <a name="BKMK_Jul15"></a>July 2015
July updates for Intune are limited to behind-the-scenes enhancements that allow us to continue providing you with a high-quality service experience. New features are not included in this service update.

Android

#### Intune Onboarding benefit
Microsoft offers the Intune Onboarding benefit for eligible plans. The Onboarding benefit lets you work remotely with Microsoft specialists to get your Intune environment ready for use. For more information, see [Microsoft Intune Onboarding benefit description](https://technet.microsoft.com/library/mt228266.aspx).

#### Changes and updates to Microsoft Company Portal apps
The following changes have been made to the company portal apps in this release:

**Android**

- Microsoft automatically collects anonymous data about the performance and use of the company portal to improve Microsoft products and services. End users can turn off data collection by using the Usage Data setting on their device, but administrators have no control over the data collection and cannot change the end user’s selection for this setting.

### <a name="BKMK_Jun15"></a>June 2015

### Help us improve Intune
In an effort to learn from you, the Intune community, about how we can improve Intune, we've set up a new feedback site powered by UserVoice. The feedback link at the bottom of the Admin console will take you to UserVoice where you can provide feedback to Microsoft on existing Intune features and content, request new features or content, and vote on submissions (help us prioritize!).

![](../Image/Intune_feedback.1.png)

### Managing the new Outlook app for iOS and Android
You can use a mobile app  management (MAM) policy to manage the new Outlook app for iOS and Android.  For a full list of apps you can apply a MAM policy to, see  [Microsoft apps you can use with Microsoft Intune mobile application management policies](../Topic/Microsoft_apps_you_can_use_with_Microsoft_Intune_mobile_application_management_policies.md).

This app is also supported by conditional access to Exchange email.  To learn more, see [Manage access to email and SharePoint with Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md).

### Updates to Endpoint Protection
**Endpoint Protection malware workspace now displays recent detection paths**
The **All Malware** page of the Protection workspace now includes a column that displays **Recent Detection Paths**. This column lists the last ten locations of the specified malware found on the computer. See [Help secure Windows PCs with Endpoint Protection for Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md) for more information.

**Windows Defender management for Windows 10 Technical Preview**
Intune adds management settings for Windows Defender. Windows Defender provides malware protection and replaces Endpoint Protection in Windows 10 Technical Preview. See [Help secure Windows PCs with Endpoint Protection for Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md) for more information.

### Improved end-user experience
**Conditional access**

- A simplified email message is sent to the end-user when their mobile device is blocked.

- The number of steps the end-user needs to go through to unblock their email has been reduced.

### Changes and updates to Microsoft Company Portal apps
The following changes have been made to the company portal apps in this release:

**Windows and Windows Phone**

- Administrators can use a PowerShell script to sign the Windows Phone 8.1 Company Portal appx package with their own Symantec code-signing certificate in order to help sideload the Company Portal App. The script is distributed as part of the **WinPhoneSSPBootstrapper.exe** that is available in the [Download Center](http://www.microsoft.com/download/details.aspx?id=46445).

- Bug fixes

**iOS**

- The Microsoft Intune Company Portal app for iOS has been updated to support iOS version 7.1 and later. This update means that end users can enroll new devices in Intune only if the device is running iOS version 7.1 or later. Devices that are running iOS version 7.0 or earlier cannot be enrolled. Users who have already enrolled devices that are running on an unsupported version of iOS can continue to use the Company Portal app that is on their device.

- Improved app catalog experience for discovering and installing company apps

- Bug fixes

### What's new in Intune documentation -- June 2015

#### Updated topics

|Name <br /> <br />|Details <br /> <br />|
|--------|-----------|
|[Microsoft apps you can use with Microsoft Intune mobile application management policies](../Topic/Microsoft_apps_you_can_use_with_Microsoft_Intune_mobile_application_management_policies.md) <br /> <br />|Updated with the latest managed apps you can use with mobile application management policies. <br /> <br />|
|[Manage access to email and SharePoint with Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md) <br /> <br />|Updated with the latest apps that support conditional access to Exchange email and SharePoint Online. <br /> <br />|
|[Configure and deploy mobile application management policies in the Microsoft Intune console](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md) <br /> <br />|Updated with details about apps that support ‘multi identity’ which allows you to manage only corporate data for the app and not the user’s personal data. <br /> <br />|

### <a name="BKMK_May15"></a>May 2015

#### Mobile application management
The new **Microsoft Intune App Wrapping Tool for Android** lets you modify the behavior of in-house Android apps so that you can control them with mobile application management policies. For details, see [Prepare Android apps for mobile application management with the Microsoft Intune App Wrapping Tool](../Topic/Prepare_Android_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md).

**Deploy Google Play Store apps as Required**.  You can now deploy Android apps from the Google Play store as Required installations. When the app is deployed, the end user will see a notification that the app is required. When the user taps the notification, they will be brought to the Google Play Store to install the app. From the Microsoft Intune console, you can monitor whether the user has installed the app.

**Publish and deploy iOS apps without the manifest file**.  When you publish or deploy an iOS app, you now only need to specify an app installation file. The associated manifest file (.plist) is no longer required.

#### Intune policies

- Settings from the mobile device security policy have now been separated into configuration policies for each device platform. Although you can still use the mobile device security policy, and existing policies you deployed will still work, the new configuration policies contain the most up to date settings, and you should plan to migrate to using these. The new policies are:

   - Android configuration policy

   - iOS configuration policy

   - Windows configuration policy

   - Windows Phone configuration policy

   - Exchange ActiveSync policy

- The **Windows Phone OMA-URI** policy is now called the **Windows Phone custom policy**.

- A new policy, the **Windows 10 custom policy**, lets you create and deploy OMA-URI settings to control settings on enrolled Windows 10 devices.

   For details, see [Windows 10 custom policy settings in Microsoft Intune](../Topic/Windows_10_custom_policy_settings_in_Microsoft_Intune.md). For a list of settings you can use, see [Custom URI settings for Windows 10 devices](../Topic/Custom_URI_settings_for_Windows_10_devices.md).

#### New console filter – ‘Helpdesk – Groups Node’
When you apply the **Helpdesk – Groups Node** designation to an Intune service administrator, that administrator can only see a limited view of the Intune console and perform limited tasks like running malware scans, or resetting passwords. For details, see [Control what admins can see in the Microsoft Intune admin console](../Topic/Control_what_admins_can_see_in_the_Microsoft_Intune_admin_console.md).

#### Subscribe to service health notifications
Subscribe to RSS feeds on the [Intune Service Status](http://status.manage.microsoft.com/StatusPage/ServiceDashboard) page to be notified about problems with the service and upcoming maintenance.

#### Conditional access
Changes to improve the flow that end-users must navigate to make their device compliant and access email.

#### Changes and updates to Microsoft Company Portal apps
The following changes have been made to the company portal apps in this release:

**Windows and Windows Phone**

When end users are installing an app from the Windows Phone Company Portal, they can see the status of their installation in the App Details view. The three possible statuses that display are:

- Installing

- Installed

- Failed to install

**iOS**

- Bug fixes to improve security

**Android**

- Bug fixes

### What’s new in Intune documentation -- May 2015

#### New topics

|Name <br /> <br />|Details <br /> <br />|
|--------|-----------|
|[iOS configuration policy settings in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Android configuration policy settings in Microsoft Intune](../Topic/Android_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Windows configuration policy settings in Microsoft Intune](../Topic/Windows_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Windows Phone configuration policy settings in Microsoft Intune](../Topic/Windows_Phone_configuration_policy_settings_in_Microsoft_Intune.md) <br /> <br />[Exchange ActiveSync policy settings in Microsoft Intune](../Topic/Exchange_ActiveSync_policy_settings_in_Microsoft_Intune.md) <br /> <br />|Contain details about the new platform-specific configuration policies that let you control security, kiosk mode, and app compliance settings. <br /> <br />|
|[Windows 10 custom policy settings in Microsoft Intune](../Topic/Windows_10_custom_policy_settings_in_Microsoft_Intune.md) <br /> <br />|This new policy lets you control certain device settings by using OMA-URI settings. <br /> <br />|
|[Custom URI settings for Windows 10 devices](../Topic/Custom_URI_settings_for_Windows_10_devices.md) <br /> <br />|Contains a list of the OMA-URI settings that you can deploy using a Windows 10 custom policy. <br /> <br />|
|[Prepare Android apps for mobile application management with the Microsoft Intune App Wrapping Tool](../Topic/Prepare_Android_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md) <br /> <br />|This tool lets you modify the behavior of in-house Android apps so that you can control them with mobile application management policies. <br /> <br />|
|[Control what admins can see in the Microsoft Intune admin console](../Topic/Control_what_admins_can_see_in_the_Microsoft_Intune_admin_console.md) <br /> <br />|Explains the preset designations you can apply to service administrators such as staff who work on the helpdesk. These can help you delegate administrative tasks while still ensuring the security of your [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] infrastructure. <br /> <br />|

#### Updated topics

|Name <br /> <br />|Details <br /> <br />|
|--------|-----------|
|[Manage settings and features on your devices with Microsoft Intune policies](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md) <br /> <br />|Added information to help you choose the right security policy to use. <br /> <br />|
|[Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md) <br /> <br />|Updated to list all new [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] policies. Additionally, the procedures in the topic are updated to include the latest information. <br /> <br />|
|[Mobile Device Management Capabilites in Microsoft Intune [replacement]](http://msdn.microsoft.com/en-us/library/6b2f4ca9-5861-4fa0-8888-eba4cea25025) <br /> <br />|Updated to include information about the latest product capabilities. <br /> <br />|
|[What to tell your end users about using Microsoft Intune](../Topic/What_to_tell_your_end_users_about_using_Microsoft_Intune.md) <br /> <br />|Describes how IT Pros can now deploy Android apps from the Google Play Store as Required installations. <br /> <br />|

### <a name="BKMK_Apr15"></a>April 2015

#### Conditional access

- Conditional access for On-Premises Exchange now supports devices that run Android.

- You can now specify the account that will be used to send notification emails about device blocking for a conditional access policy for On-premises Exchange.

- Updates to the conditional access documentation to incorporate the latest information.

See [Manage access to email and SharePoint with Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md) for more information.

#### Configuration policies

- The new **Android custom policy** lets you deploy OMA-URI settings to Android devices that cannot be configured with a mobile device security policy. In this release, you can deploy Wi-Fi profiles that use a pre-shared key to Android devices. See [Android custom policy settings in Microsoft Intune](../Topic/Android_custom_policy_settings_in_Microsoft_Intune.md) for more information.

#### Mobile application management

- The list of available policy managed apps has been updated to include the latest information. See [Configure and deploy mobile application management policies in the Microsoft Intune console](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md) for more information.

#### Manage software
You can now deploy software to Windows Phone 8.1 devices in **.appx bundle** format. For details, see [Deploy apps to mobile devices in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune.md).

#### Windows Defender management for Windows 10 Technical Preview
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] adds management settings for Windows Defender. Windows Defender provides malware protection and replaces Endpoint Protection in Windows 10 Technical Preview. See [Help secure Windows PCs with Endpoint Protection for Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md) for more information.

#### Changes and updates to the Microsoft Company Portal apps
The following changes have been made to the company portal apps in this release:

##### Windows and Windows Phone

- Bug fixes

##### iOS

- Users can now access license terms from within the app

- The **Profile** view has been redesigned

- Bug fixes to improve security

### <a name="BKMK_Mar15"></a>March 2015

#### Device Enrollment Program (DEP) support
Intune mobile device management can now manage iOS devices purchased through Apple’s Device Enrollment program. This allows for over-the-air management of corporate-owned iOS mobile devices. For details, see [Enroll corporate-owned iOS devices in Microsoft Intune](../Topic/Enroll_corporate-owned_iOS_devices_in_Microsoft_Intune.md).

#### Limit device enrollment
Administrators can limit the number of devices each user can enroll to be managed with [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. For details, see “Set device enrollment limits” in [Enable mobile device enrollment with the Microsoft Intune Account Portal](../Topic/Enable_mobile_device_enrollment_with_the_Microsoft_Intune_Account_Portal.md).

#### Manage software
You can now deploy software to Windows Phone 8.1 devices in **.appx** format. For details, see [Deploy apps to mobile devices in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune.md).

#### Changes and updates to the Microsoft Company Portal apps
The following changes have been made to the company portal apps in this release:

##### Windows and Windows Phone

- Improved login experience on the Windows and Windows Phone Company Portal apps by using Active Directory Authentication Library (ADAL) Integration

- Bug fixes

##### Android

- Added support for Wi-Fi profiles with passkeys when Intune is used with Configuration Manager

- Added Support for **Remote Lock** and **Passcode Reset** features when [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. is used with [!INCLUDE[cmshort](../Token/cmshort_md.md)].

- Added a **Verbose Logging** setting to improve troubleshooting

- Improved performance of SCEP certificate profiles

- Bug fixes

### <a name="BKMK_Feb15"></a>February 2015

#### Conditional access

- The new SharePoint Online policy lets you prevent apps from accessing SharePoint Online when the device is not compliant.

#### Wi-Fi profiles
Use the new **Windows Wi-Fi Import Policy** to import a set of Wi-Fi settings (for Windows 8.1 and later) that you can then deploy to device and user groups in your organization.

For details, see [Help users connect to company networks using Wi-Fi profiles with Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md).

#### VPN profiles
Per-app VPN connections are now supported for iOS devices when the connection type is Cisco AnyConnect.

#### Mobile device security policy settings
The following functionality has changed for mobile device security policy settings:

- When you enable the setting **Require automatic updates**, you can now also select the minimum category of updates you want to automatically install.

- The **Require encryption on mobile devices**  setting now supports Windows 8.1. When you enable this setting, users must connect their Microsoft Account to the device.

For details, see [Manage settings and features on your devices with Microsoft Intune policies](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md).

#### Mobile application management
Added information about the latest apps you can manage by using mobile application management policies to the [Configure and deploy mobile application management policies in the Microsoft Intune console](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md) topic.

### <a name="BKMK_Dec14"></a>December 2014

#### Conditional access
Conditional access, introduced in the November 2014 release now contains the following new capabilities:

- Conditional access policies can now be used to control access to Exchange Online.

- Create compliance policies that define the rules and settings that a device must comply with to access Exchange On-premises and Exchange Online.

For details, see [Manage access to email and SharePoint with Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md).

#### Manage corporate-owned iOS devices
[Enroll corporate-owned iOS devices in Microsoft Intune](../Topic/Enroll_corporate-owned_iOS_devices_in_Microsoft_Intune.md). With this enrollment method users cannot un-enroll or factory reset the device. The administrator preconfigures iOS devices in one of two ways:

- Sets up the devices for enrollment and then distributes each device to a single user, also known as “choose your own device” (CYOD)

- Enrolls the device to be user-less and shared amongst a group of users such as point-of-sale devices in a restaurant

#### Mobile application management
Managed mobile apps work with mobile application management policies to restrict certain app operations such as copy and paste, or screenshot functionality.

- [Prepare iOS apps for mobile application management with the Microsoft Intune App Wrapping Tool](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md) – This tool lets you configure your in-house iOS apps to work with mobile application management policies.

- Use mobile application management policies to apply settings to compatible apps that let you restrict the functionality of the app. For details, see [Configure and deploy mobile application management policies in the Microsoft Intune console](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md).

- The managed browser is a web browser you can deploy to your devices that lets you control the sites that users are allowed to visit. You can additionally apply mobile application management policies to the browser. For details, see [Manage Internet access using managed browser policies with Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md).

#### Custom settings policies
For mobile device settings that cannot be configured by a mobile device security policy, you can create custom policies for iOS devices that you have exported from the Apple Configurator tool. For details, see [iOS custom policy settings in Microsoft Intune](../Topic/iOS_custom_policy_settings_in_Microsoft_Intune.md).

For devices that run Windows Phone, you can create and deploy a policy that contains OMA-URI settings to control features on the device.

#### Monitoring and reporting
A new report, **Device History**, lets you view a record of retire, wipe and delete actions. You can use this report to see who initiated actions on devices in the past.

### <a name="BKMK_Nov14"></a>November 2014
In addition to the following, review [Network infrastructure requirements for Microsoft Intune](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md) for recent changes.

#### Product name change
With this release, Windows Intune is now called [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

#### Intune admin console improvements
A number of improvements have been made to the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] admin console including a new **Dashboard** page that provides quick access to status details that help you manage [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] and find details about your managed devices. For details about the admin console, see [Reference for the Microsoft Intune administrative consoles](../Topic/Reference_for_the_Microsoft_Intune_administrative_consoles.md).

#### Conditional access to on-premises Exchange

- Let’s you block access to on-premises Microsoft Exchange email from mobile devices, if the device is not managed by [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. For details, see [Manage access to email and SharePoint with Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md).

#### Company resource access

- **Certificate profiles** – Lets you provision and deploy authentication certificates for managed devices to help users seamlessly access company resources using VPN and Wi-Fi profiles. For details, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).

- **Email profiles** – You can now create and deploy email profiles for devices that run Samsung KNOX. For details, see [Configure access to corporate email using email profiles with Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md).

- **VPN profiles** – Lets you create and deploy VPN settings, minimizing the end-user effort required to connect to resources on the company network. You can also associate VPN profiles with a managed app, so that it automatically opens a VPN connection when the app runs. For details, see [Help users connect to their work using VPN profiles with Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md).

- **Wi-Fi profiles** – Lets you create and deploy Wi-Fi settings, minimizing the end-user effort required to connect to the corporate Wi-Fi network. For details, see [Help users connect to company networks using Wi-Fi profiles with Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md).

#### Manage software

- **Managed mobile apps for iOS** - Use the **Managed iOS app from the app store** installation type to manage and deploy iOS apps that are free of charge from the app store. You can deploy this installer type as a required install to make it mandatory on managed devices, or deploy it as available to let users download it from the app store. You can also associate app restrictions with compatible apps and review their status in the admin console. For details, see [Plan for app deployment in Microsoft Intune](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md).

- **Required app install and uninstall** – The deployment action of **Required** is now supported by mobile devices. For details, see [Understand software deployment actions](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_Depl).

- **App updates** – Update an app with a new revision and automatically deploy this to devices. For details, see [Deploy apps to mobile devices in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune.md) and [Deploy apps to Windows PCs in Microsoft Intune](../Topic/Deploy_apps_to_Windows_PCs_in_Microsoft_Intune.md).

#### Data protection

- **Remote passcode reset** is now supported by Windows Phone 8 and Windows Phone 8.1. For details, see [Help protect your data with remote wipe, remote lock, or passcode reset using Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md).

- **Multi-Factor Authentication** is now supported by [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. For details, see [Protect Windows devices with multi-factor authentication in Microsoft Intune](../Topic/Protect_Windows_devices_with_multi-factor_authentication_in_Microsoft_Intune.md).

- **Filtered groups** - Let you restrict the management actions an IT admin in your organization can take to only the groups you specify. For details, see [Use groups to manage users and devices with Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

#### Bulk enrollment

- Device enrollment manager allows an Intune user to enroll more than 5 mobile devices. In addition to enrolling devices, the device enrollment manager can install company apps and software, and configure access to the managed devices. For details, see [Enroll corporate-owned devices with the Device Enrollment Manager in Microsoft Intune](../Topic/Enroll_corporate-owned_devices_with_the_Device_Enrollment_Manager_in_Microsoft_Intune.md).

#### Configuration policies
Configuration policies provide the following capabilities:

- **Compliant and noncompliant apps** – Lets you specify a list of apps that users can, and cannot install.

- **Kiosk mode** - Lets you to lock a device to only allow certain features to work. For example, you can allow a device to only run one managed app that you specify, or you can disable the volume buttons on a device.

For details, see [iOS configuration policy settings in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md).

#### Terms and conditions

- When you publish terms and conditions, your users will see these when they first use the company portal from any device, whether or not that device is already enrolled. Users will have to accept those terms to access the portal. For details, see [About Terms and Conditions](../Topic/Enable_mobile_device_enrollment_with_the_Microsoft_Intune_Account_Portal.md#BKMK_TermsAndConditions).

### <a name="BKMK_Sep14"></a>September 2014

#### Email Profiles
Email profiles help you create, deploy and monitor Exchange ActiveSync email settings on devices. This lets user’s access corporate email on their personal devices without any required setup on their part. For more information, see [Configure access to corporate email using email profiles with Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md).

#### New Mobile Device Policy Settings
New policy settings have been added to help you manage more features on your managed mobile devices. For more information, see [Mobile device management capabilities in Microsoft Intune](../Topic/Mobile_device_management_capabilities_in_Microsoft_Intune.md).

### <a name="bkmk_ape"></a>April 2014

#### Windows Phone 8.1
Windows Phone 8.1 is now supported. Windows Phone 8.1 which comes with support for new policy settings.

#### Android Samsung KNOX
Android Samsung KNOX is now supported and supports selective wipe.

#### Wipe for EFS-enabled content
You can now wipe EFS-enabled content such as content relating the Mail app for Windows. For more information, see [Help protect your data with remote wipe, remote lock, or passcode reset using Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md).

### <a name="bkmk_Jan2014"></a>January 2014

#### Remote Lock and Passcode Reset for Devices
You can lock mobile devices remotely and also reset the passcode. For more information, see [Help protect your data with remote wipe, remote lock, or passcode reset using Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md).

#### Featured Apps
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] now allows you to configure an app as a featured app. This app will then be displayed prominently in the company portal. For more information, see [Deploy apps to mobile devices in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune.md).

#### Microsoft Intune Endpoint Protection Installed by Default
In the previous release of [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Endpoint Protection was only installed if a policy was created to require this installation on newly enrolled clients. In the current release of [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], the endpoint protection client is installed on computers with [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], unless a policy is created to prevent this installation. This change was made in response to customer feedback, and to better secure computers running [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. For more information, see [Help secure Windows PCs with Endpoint Protection for Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).

#### The following January 2014 updates apply to Microsoft Intune standalone only and do not require Configuration Manager

##### New Mobile Device Policy Settings
New policy settings have been added to help you manage more features on your inventoried mobile devices.  For more information, see [Get ready to enroll devices in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md).

##### New Mobile Device Inventory Report
A new report type has been added specifically to report on inventoried mobile devices in your organization.  For more information, see [Understand Microsoft Intune operations by using reports](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md).

##### Web Apps
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] now allows you to deploy a shortcut to an application on the Web to your devices. For more information, see [Plan for app deployment in Microsoft Intune](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md).

##### Android Support
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] now lets you enroll Android devices for direct management. For more information, see [Set up Android management with Microsoft Intune](../Topic/Set_up_Android_management_with_Microsoft_Intune.md).

### <a name="bkmk_Oct2013"></a>October 2013

#### Windows 8.1 Support
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] now supports Windows 8.1 devices, including Windows Professional, Surface, Surface Pro, and Windows Phone.

#### Enroll Clients with Device Management on Windows 8.1
Devices running Windows 8.1 and Windows RT 8.1 can now enable Device Management and automatically enroll and install apps. For more information, see [Enable mobile device enrollment with the Microsoft Intune Account Portal](../Topic/Enable_mobile_device_enrollment_with_the_Microsoft_Intune_Account_Portal.md).

#### “Ungrouped Devices” group added back to Administrator Console
The default “Ungrouped Devices” group, which was removed in a previous version, is back. Newly enrolled devices are automatically assigned to this group.

#### New Company Portal App for iOS Devices
iOS devices can now use their own fully featured company portal app, instead of the mobile web app.

#### New Policy Settings for Microsoft Intune Client Agent Updates
Two new policy settings have been added to help administrators streamline client agent updates:

- **Prompt user to restart Windows during Microsoft Intune client agent mandatory updates**.

- **Microsoft Intune client agent mandatory updates installation schedule**, with the parameters **Day scheduled**, and **Time scheduled**.

#### New Policy Setting for Installing Endpoint Protection
A new value has been added to the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Agent policy setting **Install Endpoint Protection**. The new value is **No**, and is the default value.

> [!NOTE]
> This behavior is different than previous version of [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], where [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Endpoint Protection was installed automatically during client installation. After upgrading, you may need to create a new policy to ensure that new clients will have Endpoint Protection installed, and that existing clients will continue to receive updates.  .

### <a name="bkmk_June2013"></a>June 2013

#### Service to Service Connector for Exchange
With this update, you can now configure the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Exchange Connector to connect directly from your [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] service to your hosted Exchange environment, without downloading additional software.  .

#### Support Tool for Microsoft Intune Trial Management of Window Phone 8
This tool makes it easy to try out Windows Phone 8 device management using Microsoft System Center 2012 Configuration Manager during your [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] subscription trial period, without having to procure a Symantec certificate. This tool contains:

- A script that populates a sample Application Enrollment token.

- A sample Windows Phone 8 company portal app.

- Two sample applications that can be used for Windows Phone 8 software distribution scenarios.

The Support Tool for [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Trial Management of Window Phone 8 can be downloaded from the [Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=39079).

### <a name="bkmk_May2013"></a>May 2013

#### Microsoft Intune administrator console sessions limited to 8 hours
With this security update, once you log in to the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] administrator console, your session will become invalid after eight hours and you will be prompted to log in again.

### <a name="bkmk_April2013"></a>April 2013

#### Install a Windows 8 or Windows RT app by scanning a Microsoft Tag or Bar Code
With this update, you can now scan a Microsoft Tag or bar code and automatically navigate to the app details page in the Windows 8 or Windows RT company portal app.  If the company portal app is not installed, you will be prompted to install it.

### <a name="bkmk_March2013"></a>March 2013

#### Exchange Connector Support for Office 365
With this update, you can now configure the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Exchange connector to connect to your hosted Exchange environment in Office 365.  For more information, see [Mobile device management with Exchange ActiveSync and Microsoft Intune](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md)

#### Share an app from your Windows Phone 8
With this update you can share an app with another person by selecting **Share** from the app details page. This will send an email with a direct link to the app details page.  You do not need to have the app installed yourself to share the app.

#### Install a Windows Phone 8 app by scanning a Microsoft Tag or Bar Code
With this update, you can now scan a Microsoft Tag or bar code and automatically navigate to the app details page in the Windows Phone 8 company portal app.  If the company portal app is not installed, you will be prompted to install it.

## See Also
[Start using Microsoft Intune](../Topic/Start_using_Microsoft_Intune.md)
[Microsoft Intune TechNet Library](http://go.microsoft.com/fwlink/?LinkID=247636)
[Microsoft Intune Product Information](http://go.microsoft.com/fwlink/?LinkID=249135)
[Microsoft Intune Blog](http://go.microsoft.com/fwlink/?LinkID=273882)

