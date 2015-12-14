---
description: na
keywords: na
pagetitle: iOS custom policy settings in Microsoft Intune
search: na
ms.author: dbdc710f437843008017318979c6adba
ms.date: 2015-10-08
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 04e60d5a-3da6-4943-b6ff-e6a331bcbcfa
---
# iOS custom policy settings in Microsoft Intune
Use the [!INC[wit_firstref](../Token/wit_firstref_md.md)]**iOS custom configuration policy** to deploy settings that you created using the [Apple Configurator tool](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) to iOS devices. This tool lets you create many settings that control the operation of these devices and export them to a configuration profile. You can then import this configuration profile into a [!INC[wit_nextref](../Token/wit_nextref_md.md)] iOS custom policy and deploy the settings to users and devices in your organization.

This capability is intended to allow you to deploy iOS settings that are not configurable with [!INC[wit_nextref](../Token/wit_nextref_md.md)] policies. For information about the settings you can configure with these policies, see [iOS configuration policy settings in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md).

## Prerequisites
Before you start, you must have installed the Apple Configurator and created a configuration file containing the settings you want to deploy to users or devices. You can download and learn about the Apple Configurator from [the Mac App Store](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12)

> [!NOTE]
> [!INC[wit_nextref](../Token/wit_nextref_md.md)] does not report the compliance of individual settings in an iOS custom policy. However, the overall compliance of the policy is reported.

## How to create an iOS custom policy

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Policy** &gt; **Overview** &gt; **Add Policy**.

2. Configure a policy of the type **iOS** &gt; **Custom Configuration**.

   For help creating and deploying policies, see [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

   You can only create and deploy a custom iOS custom policy. Recommended settings are not available.

3. Use the following table to help you configure the policy settings:

   |Setting name <br /> <br />|More information <br /> <br />|
   |----------------|--------------------|
   |**Name** <br /> <br />|Enter a unique name for the iOS custom policy to help you identify it in the [!INC[wit_nextref](../Token/wit_nextref_md.md)] console. <br /> <br />|
   |**Description** <br /> <br />|Provide a description that gives an overview of the iOS custom policy and other relevant information that helps you to locate it. <br /> <br />|
   |**Custom configuration profile name (displayed to users)** <br /> <br />|Provide a name for the policy as it will be displayed on the device, and in [!INC[wit_nextref](../Token/wit_nextref_md.md)] policy reports. <br /> <br />|
   |**Configuration profile file** <br /> <br />|Click **Import**, then browse to the configuration profile that you created using the Apple Configurator. **Note:** Ensure that the settings you export from the Apple Configurator tool are compatible with the version of iOS on the devices to which you deploy the iOS custom policy. For information about how incompatible settings are resolved, search for **Configuration Profile Reference** and **Mobile Device Management Protocol Reference** on the [Apple Developer](https://developer.apple.com/) web site. <br />|
   |**Configuration profile details** <br /> <br />|Displays the xml code for the configuration profile that you imported. <br /> <br />|

4. When you are finished, click **Save Policy**.

5. The new policy displays in the **Configuration Policies** node of the **Policy** workspace.

## Deploy an iOS custom policy

- Deploy the iOS custom policy to one or more groups of users or devices in your organization.

For help deploying policies, see [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

A status summary and alerts on the **Overview** page of the **Policy** workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the **Dashboard** workspace.

## See Also
[Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

