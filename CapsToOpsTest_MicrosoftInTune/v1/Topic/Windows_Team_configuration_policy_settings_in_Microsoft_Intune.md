---
description: na
keywords: na
pagetitle: Windows Team configuration policy settings in Microsoft Intune
search: na
ms.author: dbdc710f437843008017318979c6adba
ms.date: 2015-11-23
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 38194ef3-e26e-4682-958d-14b395fccba1
---
# Windows Team configuration policy settings in Microsoft Intune
Use the [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**Windows 10 Team general configuration policy** to configure settings for enrolled Windows 10 Team devices such as the Microsoft Surface Hub.

## Create a Windows 10 Team configuration policy

#### To provide basic settings for the configuration policy

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Policy** &gt; **Overview** &gt; **Add Policy**.

2. Click **Windows** &gt; **General Configuration (Windows 10 Team and later)** and then click **Create Policy**.

   > [!NOTE]
   > You cannot create a configuration policy using recommended settings. You must create a custom policy.

3. In the **General** section of the **Create Policy** page, specify a name and a description for the new policy.

4. Use the information in the following section to help you supply settings for the policy.

5. When you are finished, click **Save Policy**.

The new policy displays in the **Configuration Policies** node of the **Policy** workspace.

## <a name="BKMK_Settings"></a>List of settings for this policy

### <a name="BKMK_sec"></a>Device settings

|Setting name <br /> <br />|Details <br /> <br />|
|----------------|-----------|
|**Allow screen to wake automatically when someone in the room** <br /> <br />|Allows the device to wake automatically when its sensor detects someone in the room. <br /> <br />|
|**Require PIN for wireless projection** <br /> <br />|Specifies whether you must enter a PIN before you can use the wireless projection capabilities of the device. <br /> <br />|
|**Set a maintenance window for device updates** <br /> <br />|Configures the window when updates can take place to the device. You can configure the start time of the window and the duration (from 1-5 hours). <br /> <br />|
|**Enable Azure Operational Insights** <br /> <br />|Azure Operational Insights , part of the Microsoft Operations Manager suite collects, stores, and analyzes log file data from Windows 10 Team devices. <br /> <br />To connect to Azure Operational insights, you must specify a **Workspace ID** and a **Workspace Key**. <br /> <br />|
|**Enable Miracast wireless projection** <br /> <br />|Enable this option if you want to let the Windows 10 Team device use Miracast enabled devices to project. <br /> <br />If you enable this option, from **Choose Miracast channel** select the Miracast channel used to project content. <br /> <br />|
|**Choose the meeting information displayed on the welcome screen** <br /> <br />|If you enable this option, you can choose the information that will be displayed on the **Meetings** tile of the **Welcome** screen. You can: <br /> <br /><ul><li>**Show organizer and time only** </li><li>**Show organizer, time and subject (subject hidden for private meetings)** </li> </ul>|
|**Lockscreen background image URL** <br /> <br />|Enable this setting to display a custom background on the **Welcome** screen of Windows 10 Team devices from the URL you specify. <br /> <br />The image must be in PNG format and the URL must begin with **https://**. <br /> <br />|

## Deploy the Configuration Policy

1. Deploy the configuration policy to one or more groups of users or devices in your organization.

For more information about how to deploy policies, see [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

A status summary and alerts In the **Policy** workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the **Dashboard** workspace.

## See Also
[Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

