---
description: na
search: na
title: Windows 10 configuration policy settings in Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-17
ms.author: dbdc710f437843008017318979c6adba
---
# Windows 10 configuration policy settings in Microsoft Intune
Use the [!INC[wit_firstref](../Token/wit_firstref_md.md)]**general configuration policy** for Windows 10 to configure settings for enrolled Windows 10 desktop, and Windows 10 Mobile devices:

## Create a Windows 10 general configuration policy

#### To provide basic settings for the configuration policy

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Policy** &gt; **Overview** &gt; **Add Policy**.

2. Click **Windows** &gt; **General Configuration (Windows 10 Desktop and Mobile and later)** and then click **Create Policy**.

   > [!NOTE]
   > You cannot create a configuration policy using recommended settings. You must create a custom policy.

3. In the **General** section of the **Create Policy** page, specify a name and a description for the new policy.

4. Use the information in the following sections to help you supply settings for the policy.

5. When you are finished, click **Save Policy**.

The new policy displays in the **Configuration Policies** node of the **Policy** workspace.

## Security settings

### Password

|Setting name <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|----------------------|---------------------|
|**Require a password to unlock devices** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Required password type** <br /> <br />(Specifies the type of password that will be required, such as numeric only, or alphanumeric) <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Required password type** - **Minimum number of character sets** <br /> <br />(There are four character sets, lowercase letters, uppercase letters, numbers, and symbols. This setting specifies how many different character sets must be included in the password). <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Minimum password length (Windows 10 Desktop only)** **Important:** This setting is no longer supported and will be removed in the future. You can use the setting for Windows 10 Mobile below for desktop computers. <br />|Yes <br /> <br />|No <br /> <br />|
|**Minimum password length (Windows 10 Mobile only)** <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|**Number of repeated sign-in failures to allow before the device is wiped** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Minutes of inactivity before screen turns off** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Password expiration (days)** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Remember password history** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Remember password history** - **Prevent reuse of previous passwords** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow picture password and PIN** <br /> <br />Lets you use simple gestures on a picture, or a simple PIN to login. <br /> <br />|Yes <br /> <br />|No <br /> <br />|
|**Require a password when the device returns from an idle state** <br /> <br />|No <br /> <br />|Yes <br /> <br />|

### Encryption

|Setting name <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|----------------------|---------------------|
|**Require encryption on mobile device** <br /> <br />|No <br /> <br />|Yes <br /> <br />|

### System

|Setting name <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|----------------------|---------------------|
|**Allow screen capture** <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|**Allow manual unenrollment** <br /> <br />Lets the user manually delete the workplace account from the device. <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow manual root certificate installation** <br /> <br />Specifies whether the user can manually install root certificates <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|**Allow diagnostic and usage data to be sent to Microsoft** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|

## Cloud settings

### Account and synchronization

|Setting name <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|----------------------|---------------------|
|**Allow Microsoft account** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow adding non-Microsoft accounts manually** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow settings synchronization for Microsoft accounts** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|

## Email settings

|Setting name <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|----------------------|---------------------|
|**Make Microsoft account optional in Windows Mail application** <br /> <br />|Yes <br /> <br />|No <br /> <br />|

## Application settings

### Microsoft Edge

|Setting name <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|----------------------|---------------------|
|**Allow web browser** <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|**Allow search suggestions in address bar** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow sending intranet traffic to Internet Explorer** <br /> <br />|Yes <br /> <br />|No <br /> <br />|
|**Allow do not track** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Enable SmartScreen** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow active scripting** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow pop-ups** <br /> <br />|Yes <br /> <br />|No <br /> <br />|
|**Allow cookies** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow Autofill** <br /> <br />|Yes <br /> <br />|No <br /> <br />|
|**Allow Password Manager** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Enterprise Mode site list location** <br /> <br />Specifies where to find the list of web sites that will open in Enterprise mode. Users cannot edit this list. <br /> <br />|Yes <br /> <br />|No <br /> <br />|

### Apps

|Setting name <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|----------------------|---------------------|
|**Allow application store** <br /> <br />|No <br /> <br />|Yes <br /> <br />|

## Device capability settings

### Cellular

|Setting name <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|----------------------|---------------------|
|**Allow data roaming** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow VPN over cellular** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow VPN roaming over cellular** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|

### Hardware

|Setting name <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|----------------------|---------------------|
|**Allow camera** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow removable storage** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow Wi-Fi** <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|**Allow internet sharing** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow manual Wi-Fi configuration** <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|**Allow automatic connection to free Wi-Fi hotspots** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow geolocation** <br /> <br />Specifies whether the device can use location services information. <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow NFC** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow Bluetooth** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow Bluetooth discoverable mode** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow Bluetooth advertising** <br /> <br />Allows devices to receive advertisements over Bluetooth. <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow Bluetooth connectable mode** **Important:** This setting is no longer supported by Windows 10 and will be removed in the future. <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow phone reset** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow USB connection** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow AntiTheft mode** <br /> <br />Configure whether Windows Antitheft mode is enabled. <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|

### Features

|Setting name <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|----------------------|---------------------|
|**Allow copy and paste** <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|**Allow voice recording** <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|**Allow Cortana** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|**Allow action center notifications** <br /> <br />|No <br /> <br />|Yes <br /> <br />|

## Updates settings

|Setting name <br /> <br />|Description <br /> <br />|Windows 10 Desktop <br /> <br />|Windows 10 Mobile <br /> <br />|
|----------------|---------------|----------------------|---------------------|
|**Allow automatic updates** <br /> <br />|Enable this setting to allow automatic updates. Then, configure one of the following settings to control update behavior: <br /> <br /><ul><li>**Notify download** </li><li>**Auto install at maintenance time** </li><li>**Auto install and reboot at maintenance time** </li><li>**Auto install and reboot at scheduled time** <br /> <br />   When this option is selected, you can also configure the following settings: <br /> <br /><ul><li>**Suppress notification to end user** </li><li>**Define install day for scheduled updates** </li> </ul> </li> </ul>|Yes <br /> <br />|No <br /> <br />|

## Deploy the Configuration Policy

1. Deploy the configuration policy to one or more groups of users or devices in your organization.

For more information about how to deploy policies, see [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

A status summary and alerts In the **Policy** workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the **Dashboard** workspace.

## See Also
[Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

