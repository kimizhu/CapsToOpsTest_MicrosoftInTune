---
description: na
keywords: na
pagetitle: Control Microsoft Passport settings on devices with Microsoft Intune
search: na
ms.author: dbdc710f437843008017318979c6adba
ms.date: 2015-11-23
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 402bc5a1-ada3-4c4c-a0de-292d026b4444
---
# Control Microsoft Passport settings on devices with Microsoft Intune
[!INC[wit_firstref](../Token/wit_firstref_md.md)] lets you integrate with Microsoft Passport for Work which is an alternative sign-in method that uses Active Directory, or an Azure Active Directory account to replace a password, smart card, or virtual smart card.

Passport lets you use a **user gesture** to login, instead of a password. A user gesture might be a simple PIN, biometric authentication such as Windows Hello, or an external device such as a fingerprint reader.

[!INC[wit_nextref](../Token/wit_nextref_md.md)] integrates with Passport for Work in two ways:

- You can use [!INC[wit_nextref](../Token/wit_nextref_md.md)] policy to control which gestures users can and cannot use to login

- You can store authentication certificates in the Passport for Work key storage provider (KSP). For more information, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).

## To create a Passport for Work policy

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Admin** &gt; **Mobile Device Management** &gt; **Windows** &gt; **Passport for Work**.

2. Choose from the following values that will affect all enrolled Windows 10 and Windows 10 Mobile devices:

   |Setting <br /> <br />|Description <br /> <br />|
   |-----------|---------------|
   |<ul><li>**Disable Passport for Work on enrolled devices** </li><li>**Enable Passport for Work on enrolled devices** </li> </ul>|Enables or disables the use of Passport for work on all enrolled Windows 10 and Windows 10 mobile devices. **Important:** This policy is enabled by default and applied to all Windows 10 devices when they enroll. <br />|
   |**Use a Trusted Platform Module (TPM)** <br /> <br />|A Trusted Platform Module (TPM) chip provides an additional layer of data security. <br /> <br />Choose one of the following values: <br /> <br /><ul><li>**Required** (default) - Only devices with an accessible TPM can provision Passport for Work. </li><li>**Preferred** - Devices first attempt to use a TPM. If this is not available, they can use software encryption </li> </ul>|
   |**Require minimum PIN length** <br /> <br />|Specify the minimum number of characters required for the Passport for Work PIN. You must use at least 4 characters (the default value is 6 characters). ​ <br /> <br />|
   |**Require maximum PIN length** <br /> <br />|Specify the maximum number of characters allowed for the Passport for Work PIN. You can use up to 127 characters. <br /> <br />|
   |**Require lowercase letters in PIN** <br /> <br />|Specifies whether lowercase letters must be used  in the Passport for Work PIN. Choose from: <br /> <br /><ul><li>**Allowed** - Users can use lowercase characters in their PIN. </li><li>**Required** - Users must include at least one lowercase character in their PIN. </li><li>**Not allowed** (default) - Users must not use lowercase characters in their PIN. </li> </ul>|
   |**Require uppercase letters in PIN** <br /> <br />|Specifies whether uppercase letters must be used  in the Passport for Work PIN. Choose from: <br /> <br /><ul><li>**Allowed** - Users can use uppercase characters in their PIN. </li><li>**Required** - Users must include at least one uppercase character in their PIN. </li><li>**Not allowed** (default) - Users must not use uppercase characters in their PIN. </li> </ul>|
   |**Require special characters in PIN** <br /> <br />|Specifies the use of special characters in the PIN. Choose from: <br /> <br />Special characters include: **! " # $ % &amp; ' ( ) &#42; + , - . / : ; &lt; = &gt; ? @ [ \ ] ^ _ &#96; { &#124; } ~**. <br /> <br /><ul><li>**Allowed** - Users can use special characters in their PIN. </li><li>**Required** - Users must include at least one special character in their PIN. </li><li>**Not allowed** (default) - Users must not use special characters in their PIN (this is also the behavior if the setting is not configured). </li> </ul>|
   |**PIN expiration (days)** <br /> <br />|Specifies the number of days before the device PIN must be changed. The default is 41 days. <br /> <br />|
   |**Remember PIN history** <br /> <br />|Use this setting to restrict the re-use of previously used PINS. The default is the last 5 PINS used cannot be reused. <br /> <br />|
   |**Allow biometric authentication** <br /> <br />|Enables biometric authentication such as facial recognition or fingerprint as an alternative to a PIN for Passport for Work. Users must still configure a work PIN in case biometric authentication fails. <br /> <br />If set to **Yes**, Passport for Work allows biometric authentication.  If set to **No**, Passport for Work prevents biometric authentication (for all account types). <br /> <br />|
   |**Use enhanced anti-spoofing, when available** <br /> <br />|Configures whether enhanced anti-spoofing is used on devices that support it. <br /> <br />If set to **Yes**, Windows requires all users to use anti-spoofing for facial features when supported. <br /> <br />|
   |**Use Remote Passport** <br /> <br />|If this option is set to **Yes**, users can use a remote passport to serve as a portable companion device for desktop computer authentication. The desktop computer must be Azure Active Directory joined, and the companion device must be configured with a Passport for Work PIN. <br /> <br />|

3. When you are finished, click **Save**.

## Further information
For more information about Microsoft Passport, see [Microsoft Passport guide](https://technet.microsoft.com/library/mt589441%28v=vs.85%29.aspx) in the Windows 10 documentation.

## See Also
[Protect data and devices with Microsoft Intune](../Topic/Protect_data_and_devices_with_Microsoft_Intune.md)

