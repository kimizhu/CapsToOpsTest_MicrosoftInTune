---
description: na
search: na
title: Windows Phone configuration policy settings in Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-10-08
ms.author: dbdc710f437843008017318979c6adba
capscontentguid: 83f7469c-272e-43f2-8139-b0d7bc34f43f
---
# Windows Phone configuration policy settings in Microsoft Intune
Use the [!INC[wit_firstref](../Token/wit_firstref_md.md)]**Windows Phone general configuration policy** to configure the following settings for Windows Phone 8.1 devices:

- **Mobile device security settings** – Choose from a list of predefined settings that let you control a range of features and functionality on the device.

- **Compliant and noncompliant apps** - Specify a list of apps that are compliant, or not compliant in your company. Windows Phone devices can block, or allow installation of these apps.

## Create a Windows Phone general configuration policy

#### To provide basic settings for the configuration policy

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Policy** &gt; **Overview** &gt; **Add Policy**.

2. Click **Windows** &gt; **General Configuration (Windows Phone 8.1 and later)** and then click **Create Policy**.

   > [!NOTE]
   > You cannot create a configuration policy using recommended settings. You must create a custom policy.

3. In the **General** section of the **Create Policy** page, specify a name and a description for the new policy.

4. Use the information in the following sections to help you supply settings for the policy.

5. When you are finished, click **Save Policy**.

The new policy displays in the **Configuration Policies** node of the **Policy** workspace.

## <a name="BKMK_Settings"></a>Settings for Windows Phone

### <a name="BKMK_sec"></a>Security settings

|Setting name <br /> <br />|Windows Phone 8 and Windows Phone 8.1 <br /> <br />|
|----------------|-----------------------------------------|
|**Require a password to unlock mobile devices** <br /> <br />|Yes <br /> <br />|
|**Required password type** <br /> <br />(specifies the type of password that will be required, such as numeric only, or alphanumeric) <br /> <br />|Yes <br /> <br />|
|**Required password type – Minimum number of character sets** <br /> <br />There are four character sets, lowercase letters, uppercase letters, numbers, and symbols. This setting specifies how many different character sets must be included in the password). However, for iOS devices, this specifies the number of symbol characters must be included in the password) <br /> <br />|Yes <br /> <br />|
|**Minimum password length** <br /> <br />|Yes <br /> <br />|
|**Allow simple passwords** <br /> <br />Simple passwords include ‘0000’ and ‘1234’ <br /> <br />|Yes <br /> <br />|
|**Number of repeated sign-in failures to allow before the device is wiped** <br /> <br />|Yes <br /> <br />|
|**Minutes of inactivity before screen turns off** <br /> <br />|Yes <br /> <br />|
|**Password expiration (days)** <br /> <br />|Yes <br /> <br />|
|**Remember password history** <br /> <br />|Yes <br /> <br />|
|**Remember password history** – **Prevent reuse of previous passwords** <br /> <br />|Yes <br /> <br />|

### Encryption settings

|Setting name <br /> <br />|Windows Phone 8 and Windows Phone 8.1 <br /> <br />|
|----------------|-----------------------------------------|
|**Require encryption on mobile device** <br /> <br />For Windows Phone 8 devices, you must set this to **Yes**. <br /> <br />|Yes <br /> <br />|

### System settings

|Setting name <br /> <br />|Windows Phone 8 and Windows Phone 8.1 <br /> <br />|
|----------------|-----------------------------------------|
|**Allow screen capture** <br /> <br />|Windows Phone 8.1 only <br /> <br />|
|**Allow diagnostic data submission** <br /> <br />|Windows Phone 8.1 only <br /> <br />|

### Cloud settings – accounts and synchronization

|Setting name <br /> <br />|Windows Phone 8 and Windows Phone 8.1 <br /> <br />|
|----------------|-----------------------------------------|
|**Allow Microsoft account** <br /> <br />|Windows Phone 8.1 only <br /> <br />|

### <a name="BKMK_email"></a>Email settings

|Setting name <br /> <br />|Windows Phone 8 and Windows Phone 8.1 <br /> <br />|
|----------------|-----------------------------------------|
|**Allow custom email accounts** <br /> <br />|Windows Phone 8.1 only <br /> <br />|

### <a name="BKMK_browser"></a>Application settings - browser

|Setting name <br /> <br />|Windows Phone 8 and Windows Phone 8.1 <br /> <br />|
|----------------|-----------------------------------------|
|**Allow web browser** <br /> <br />|Windows Phone 8.1 only <br /> <br />|

### <a name="BKMK_apps"></a>Application settings - apps

|Setting name <br /> <br />|Windows Phone 8 and Windows Phone 8.1 <br /> <br />|
|----------------|-----------------------------------------|
|**Allow application store** <br /> <br />|Windows Phone 8.1 only <br /> <br />|

### <a name="BKMK_hard"></a>Device capabilities settings - hardware

|Setting name <br /> <br />|Windows Phone 8 and Windows Phone 8.1 <br /> <br />|
|----------------|-----------------------------------------|
|**Allow camera** <br /> <br />|Windows Phone 8.1 only <br /> <br />|
|**Allow removable storage** <br /> <br />|Yes <br /> <br />|
|**Allow Wi-Fi** <br /> <br />|Windows Phone 8.1 only <br /> <br />|
|**Allow Wi-Fi tethering** <br /> <br />|Windows Phone 8.1 only <br /> <br />|
|**Allow automatic connection to free Wi-Fi hotspots** <br /> <br />|Windows Phone 8.1 only <br /> <br />|
|**Allow Wi-Fi hotspot reporting** <br /> <br />(send information about Wi-Fi connections to help discover nearby connections) <br /> <br />|Windows Phone 8.1 only <br /> <br />|
|**Allow geolocation** <br /> <br />(allows the device to utilize location information) <br /> <br />|Windows Phone 8.1 only <br /> <br />|
|**Allow NFC** <br /> <br />(allows operations that use near field communication) <br /> <br />|Windows Phone 8.1 only <br /> <br />|
|**Allow Bluetooth** <br /> <br />|Windows Phone 8.1 only <br /> <br />|

### Device capabilities settings - features

|Setting name <br /> <br />|Windows Phone 8 and Windows Phone 8.1 <br /> <br />|
|----------------|-----------------------------------------|
|**Allow copy and paste** <br /> <br />|Windows Phone 8.1 only <br /> <br />|

## Settings for compliant and noncompliant apps
In the **Compliant &amp; Noncompliant Apps** list, specify a list of compliant or noncompliant apps using the following information:

> [!NOTE]
> A single policy can only contain a list of compliant, or a list of noncompliant apps. You cannot specify both in the same policy.

|Setting name <br /> <br />|More information <br /> <br />|
|----------------|--------------------|
|**Block devices from opening the listed apps** <br /> <br />|Lists the apps that are not managed by Intune which users are not allowed to install and run. <br /> <br />|
|**Allow devices to install only the listed apps** <br /> <br />|Lists the apps that users are allowed to install. Users cannot install any other apps. Apps that are managed by Intune are automatically allowed. <br /> <br />|
|**Add** <br /> <br />|Adds an app to the selected list. Specify a name of your choice, optionally the app publisher, and the URL to the app in the app store. <br /> <br />[How to specify URLs to app stores](../Topic/Windows_Phone_configuration_policy_settings_in_Microsoft_Intune.md#BKMK_URL) <br /> <br />|
|**Import Apps** <br /> <br />|Imports a list of apps you have specified in a comma-separated values file. Use the format, application name, publisher, app URL in the file. <br /> <br />|
|**Edit** <br /> <br />|Let’s you edit the name, publisher and URL of the selected app. <br /> <br />|
|**Delete** <br /> <br />|Deletes the selected app from the list. <br /> <br />|
> [!IMPORTANT]
> If you specify a list of allowed apps for Windows Phone 8.1 devices, you must add the Company Portal app to this list, or else it will be blocked.

## Deploy the Configuration Policy

1. Deploy the configuration policy to one or more groups of users or devices in your organization.

For more information about how to deploy policies, see [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

A status summary and alerts In the **Policy** workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the **Dashboard** workspace.

## Reference information for compliant and noncompliant apps

### <a name="BKMK_URL"></a>How to specify URLs to app stores
To specify an app URL in the compliant and noncompliant apps list, use the following format:

From the [Windows Phone Apps+Games](http://www.windowsphone.com/en-us/store/overview) page, search for the app you want to use.

Open the app’s page, and copy the URL to the clipboard. You can now use this as the URL in either the compliant or noncompliant apps list.

**Example:** Search the store for the Skype app. The URL you use will be **http://www.windowsphone.com/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51**.

## See Also
[Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

