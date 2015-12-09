---
description: na
search: na
title: Manage%20device%20compliance%20policies%20for%20Microsoft%20Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-04
ms.author: dbdc710f437843008017318979c6adba
---
# Manage%20device%20compliance%20policies%20for%20Microsoft%20Intune
<?xml version="1.0" encoding="utf-8"?>
<developerWalkthroughDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <!--Contains 1511 information. Do not publish until 1511 is released.--><para>
      <ui>Compliance policies</ui> define the rules and settings that a device must comply with in order to be considered compliant by conditional access polices. You can also use compliance policies to monitor and remediate compliant issues with devices independently of conditional access.</para>
    <para>These rules include:</para>
    <list class="bullet">
      <listItem>
        <para>PIN and passwords</para>
      </listItem>
      <listItem>
        <para>Encryption</para>
      </listItem>
      <listItem>
        <para>Whether the device is jailbroken or rooted, or if the device is reported as unhealthy by the Windows device health attestation service.</para>
      </listItem>
      <listItem>
        <para>Whether email on the device is managed by an <token>wit_nextref</token> policy</para>
      </listItem>
    <listItem><para>Minimum OS version required - Typically this depends on your company compliance policies and security requirements. This helps to prevent access to devices that might have security vulnerabilities because they are using an older OS version.</para></listItem><listItem><para>Maximum OS version allowed - You may choose not to support the latest OS version available before testing or other reasons. You can choose to block devices that have a version later than the one you have specified.   The device will not be able to access company resources until the policy is changed.</para></listItem></list><alert class="note">
 <para>On Windows PCs, Windows Operating System version 8.1, is reported as 6.3 instead of 8.1.    If the OS version rule is set to Windows 8.1 for Windows, then the device will be reported as non-compliant even if the device has Windows OS 8.1. Make sure you are setting the right <ui>reported</ui> version of Windows for the Minimum and Maximum OS rules. The version number must match the version returned by the winver command.</para><para>  Windows Phones do not have this issue, the version is reported as 8.1 as expected. </para>
</alert>
    <para>You deploy compliance policies to users and devices. When a compliance policy is deployed to a user, then all of the users devices are checked for compliance.</para>
    <para>The following table lists the device types supported by compliance policies and how noncompliant settings are managed when the policy is used with a conditional access policy.</para>
    <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
      <thead>
        <tr>
          <TD>
            <para>Device type</para>
          </TD>
          <TD>
            <para>PIN or password configuration</para>
          </TD>
          <TD>
            <para>Device encryption</para>
          </TD>
          <TD>
            <para>Jailbroken or rooted device</para>
          </TD>
          <TD>
            <para>Email profile</para>
          </TD><TD><para>Minimum OS version</para></TD><TD><para>Maximum OS version</para></TD>
        </tr>
      </thead>
      <tbody>
        <tr>
          <TD>
            <para>Windows 8.1 and later</para>
          </TD>
          <TD>
            <para>Remediated</para>
          </TD>
          <TD>
            <para>N/A</para>
          </TD>
          <TD>
            <para>N/A</para>
          </TD>
          <TD>
            <para>N/A</para>
          </TD><TD><para>Quarantined</para></TD><TD><para>Quarantined</para></TD>
        </tr>
        <tr>
          <TD>
            <para>Windows Phone 8.1 and later</para>
          </TD>
          <TD>
            <para>Remediated</para>
          </TD>
          <TD>
            <para>Remediated</para>
          </TD>
          <TD>
            <para>N/A</para>
          </TD>
          <TD>
            <para>N/A</para>
          </TD><TD><para>Quarantined</para></TD><TD><para>Quarantined</para></TD>
        </tr>
        <tr>
          <TD>
            <para>iOS 6.0 and later</para>
          </TD>
          <TD>
            <para>Remediated</para>
          </TD>
          <TD>
            <para>Remediated (by setting PIN)</para>
          </TD>
          <TD>
            <para>Quarantined (not a setting)</para>
          </TD>
          <TD>
            <para>Quarantined</para>
          </TD><TD><para>Quarantined</para></TD><TD><para>Quarantined</para></TD>
        </tr>
        <tr>
          <TD>
            <para>Android 4.0 and later</para>
          </TD>
          <TD>
            <para>Quarantined</para>
          </TD>
          <TD>
            <para>Quarantined</para>
          </TD>
          <TD>
            <para>Quarantined (not a setting)</para>
          </TD>
          <TD>
            <para>N/A</para>
          </TD><TD><para>Quarantined</para></TD><TD><para>Quarantined</para></TD>
        </tr>
        <tr>
          <TD>
            <para>Samsung KNOX Standard 4.0 and later</para>
          </TD>
          <TD>
            <para>Quarantined</para>
          </TD>
          <TD>
            <para>Quarantined</para>
          </TD>
          <TD>
            <para>Quarantined (not a setting)</para>
          </TD>
          <TD>
            <para>N/A</para>
          </TD><TD><para>Quarantined</para></TD><TD><para>Quarantined</para></TD>
        </tr>
      </tbody>
    </table>
    <para>
      <ui>Remediated</ui> = Compliance is enforced by the device operating system (for example, the user is forced to set a PIN).  There is never a case when the setting will be noncompliant.</para>
    <para>
      <ui>Quarantined</ui> = The device operating system does not enforce compliance (for example, Android devices do not force the user to encrypt the device).  In this case:</para>
    <list class="bullet">
      <listItem>
        <para>The device will be blocked if the user is targeted by a conditional access policy.</para>
      </listItem>
      <listItem>
        <para>The company portal or web portal will notify the user about any compliance issues.</para>
      </listItem>
    </list>
  </introduction>
  <section address="BKMK_Compliance">
    <title>Step 1: Create a compliance policy</title>
    <content>
      <procedure expanded="false">
        <title/>
        <steps class="ordered">
          <step>
            <content>
              <para>In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Compliance Policies</ui> &gt; <ui>Add</ui>.</para>
            </content>
          </step>
          <step>
            <content>
              <para>On the <ui>Create Policy</ui> page, configure the settings you require:</para>
              <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
                <thead>
                  <tr>
                    <TD>
                      <para>Setting name</para>
                    </TD>
                    <TD>
                      <para>More information</para>
                    </TD>
                    <TD>
                      <para>Supported platforms</para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>Name</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Enter a unique name for the compliance policy.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>All</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Description</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Provide a description that gives an overview of the compliance policy.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>All</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Require a password to unlock mobile devices</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Require users to enter a password before they can access their device.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                        <listItem>
                          <para>Android 4.0 and later</para>
                        </listItem>
                        <listItem>
                          <para>Samsung KNOX Standard 4.0 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Allow simple passwords</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Let users create simple passwords such as ‘<userInput>1234</userInput>’ or ‘<ui>1111</ui>’.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Minimum password length</ui>
                        <superscript>1</superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>Specifies the minimum number of digits or characters that the user’s password must contain.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>Windows 8.1</para>
                        </listItem>
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                        <listItem>
                          <para>Android 4.0 and later</para>
                        </listItem>
                        <listItem>
                          <para>Samsung KNOX Standard 4.0 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Required password type</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Specifies whether users must create an <ui>Alphanumeric</ui>, or a <ui>Numeric</ui> password.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>Windows RT and Windows RT 8.1</para>
                        </listItem>
                        <listItem>
                          <para>Windows 8.1</para>
                        </listItem>
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Minimum number of character sets</ui>
                        <superscript>1</superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>If <ui>Required password type</ui> is set to <ui>Alphanumeric</ui>, this setting specifies the minimum number of character sets that the password must contain.</para>
                      <para>The four character sets are:</para>
                      <list class="bullet">
                        <listItem>
                          <para>Lowercase letters</para>
                        </listItem>
                        <listItem>
                          <para>Uppercase letters</para>
                        </listItem>
                        <listItem>
                          <para>Symbols</para>
                        </listItem>
                        <listItem>
                          <para>Numbers</para>
                        </listItem>
                      </list>
                      <para>Setting a higher number for this setting will require users to create more complex passwords.</para>
                      <para>For iOS devices, this setting refers to the number of special characters (for example, <userInput>!</userInput>, <userInput>#</userInput>, <userInput>&amp;</userInput>) that must be included in the password.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>Windows RT and Windows RT 8.1</para>
                        </listItem>
                        <listItem>
                          <para>Windows 8.1</para>
                        </listItem>
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Password quality</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Configures password requirements for Android devices. Choose from:</para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>Low security biometric</ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>Required</ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>At least numeric</ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>At least alphabetic</ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>At least alphanumeric</ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>Alphanumeric with symbols</ui>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>Android 4.0 and later</para>
                        </listItem>
                        <listItem>
                          <para>Samsung KNOX Standard 4.0 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Minutes of inactivity before password is required</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Specifies the idle time before the user must re-enter their password.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem><para>Windows Phone 8 and later</para></listItem><listItem><para>Windows RT and Windows RT 8.1</para></listItem><listItem><para>Windows 8.1</para></listItem><listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                      <listItem><para>Android 4.0 and later</para></listItem><listItem><para>Samsung KNOX Standard 4.0 and later</para></listItem></list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Password expiration (days)</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <?Comment RS: Is this select, or specify? 2015-04-03T08:34:00Z  Id='0?>Select the number of days before the user’s password expires and they must create a new one.<?CommentEnd Id='0'
    ?></para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>Windows RT and Windows RT 8.1</para>
                        </listItem>
                        <listItem>
                          <para>Windows 8.1</para>
                        </listItem>
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                        <listItem>
                          <para>Android 4.0 and later</para>
                        </listItem>
                        <listItem>
                          <para>Samsung KNOX Standard 4.0 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Remember password history</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Use this setting in conjunction with <ui>Prevent reuse of previous passwords</ui> to restrict the user from creating previously used passwords.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>Windows RT and Windows RT 8.1</para>
                        </listItem>
                        <listItem>
                          <para>Windows 8.1</para>
                        </listItem>
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                        <listItem>
                          <para>Android 4.0 and later</para>
                        </listItem>
                        <listItem>
                          <para>Samsung KNOX Standard 4.0 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Prevent reuse of previous passwords</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>If <ui>Remember password history</ui> is selected, specify the number of previously used passwords that cannot be re-used.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>Windows RT and Windows RT 8.1</para>
                        </listItem>
                        <listItem>
                          <para>Windows 8.1</para>
                        </listItem>
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                        <listItem>
                          <para>Android 4.0 and later</para>
                        </listItem>
                        <listItem>
                          <para>Samsung KNOX Standard 4.0 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr><tr><TD><para><ui>Require a password when the device returns from an idle state</ui></para></TD><TD><para>This setting should be used together with the in the <ui>Minutes of inactivity before password is required</ui> setting. The end-users will be prompted to enter a password to access a device that has been inactive for the time specified in the <ui>Minutes of inactivity before password is required</ui> setting.</para></TD><TD><list class="bullet"><listItem><para>Windows 10 Mobile</para></listItem></list></TD></tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Require encryption on mobile device</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Requires the device to be encrypted in order to connect to resources.</para>
                      <para>Devices that run Windows Phone 8 are automatically encrypted.</para>
                      <alert class="important">
                        <para>Devices that run iOS are encrypted when you configure the setting <ui>Require a password to unlock mobile devices</ui>.</para>
                      </alert>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>Android 4.0 and later</para>
                        </listItem>
                        <listItem>
                          <para>Samsung KNOX Standard 4.0 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr><tr><TD><para><ui>Require devices to be reported as healthy</ui></para></TD><TD><para>You can set a rule to require that Windows 10 devices must be reported as healthy in new or existing Compliance Policies.  If this setting is enabled, Windows 10 devices will be evaluated via the Health Attestation Service (HAS) for  the following data points:</para><list class="bullet"><listItem><para>BitLocker is enabled</para><para>When Bitlocker is on, the device is able to protect data that is stored on the drive from unauthorized access, when the system is turned off or goes to hibernation. 
Windows BitLocker Drive Encryption encrypts all data stored on the Windows operating system volume. BitLocker uses the TPM to help protect the Windows operating system and user data and helps to ensure that a computer is not tampered with, even if it is left unattended, lost, or stolen.
If the computer is equipped with a compatible TPM, BitLocker uses the TPM to lock the encryption keys that protect the data. As a result, the keys cannot be accessed until the TPM has verified the state of the computer. 
</para></listItem><listItem><para>Code integrity is enabled</para><para>Code integrity is a feature that validates the integrity of a driver or system file each time it is loaded into memory. Code integrity detects whether an unsigned driver or system file is being loaded into the kernel, or whether a system file has been modified by malicious software that is being run by a user account with administrator privileges.</para></listItem><listItem><para>Secure boot is enabled</para><para>When Secure Boot is enabled, the system is forced to boot to a factory trusted state. Also, when Secure Boot is enabled, the core components used to boot the machine must have correct cryptographic signatures that are trusted by the organization that manufactured the device. The UEFI firmware verifies this before it lets the machine start. If any files have been tampered with, breaking their signature, the system will not boot.

</para></listItem><listItem><para>Early-launch antimalware is enabled (this setting only applies to PCs.)</para><para>Early launch anti-malware (ELAM) provides protection for the computers in your network when they start up and before third-party drivers initialize.</para></listItem></list><para>This rule is turned off by default. For information on how the HAS service works, see <externalLink><linkText>Health Attestation CSP</linkText><linkUri>https://msdn.microsoft.com/en-us/library/dn934876.aspx</linkUri></externalLink>.</para></TD><TD><list class="bullet"><listItem><para>Windows 10</para></listItem><listItem><para>Windows 10 Mobile</para></listItem></list></TD></tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Device must not be jailbroken or rooted</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>If enabled, jailbroken (iOS), or rooted (Android) devices will not be compliant.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                        <listItem>
                          <para>Android 4.0 and later</para>
                        </listItem>
                        <listItem>
                          <para>Samsung KNOX Standard 4.0 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Email account must be managed by Intune</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>When this option is selected, the device will be reported as noncompliant if the user has set up an email account on the device that matches an Intune email profile that was deployed to the device by an IT admin. Intune cannot overwrite the user-provisioned profile, and therefore cannot manage it.</para>
                      <para>To ensure compliance, the user must remove the existing email settings, then, Intune can install the managed email profile.</para>
                      <para>For details about email profiles, see <link xlink:href="10f0cd61-e514-4e44-b13e-aeb85a8e53ae">Enable access to corporate email using email profiles with Microsoft Intune</link>.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Select the email profile that must be managed by Intune</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>If <ui>Email account must be managed by Intune</ui> is selected, click <ui>Select</ui> to choose the Intune email profile that devices must be managed by. The email profile must be present on the device.</para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr><tr><TD><para><ui>Require automatic updates</ui></para></TD><TD><para>Select <ui>Yes</ui> to require automatic updates.</para></TD><TD><list class="bullet"><listItem><para>Windows 8.1 and later</para></listItem></list></TD></tr><tr><TD><para><ui>Require automatic updates – Minimum classification of updates to install automatically</ui></para></TD><TD><para>Choose the classification of updates that will be installed automatically:</para><list class="bullet"><listItem><para>	<ui>Important</ui> – Installs all updates classified as important.</para></listItem><listItem><para><ui>Recommended</ui> – Installs all updates classified as important or recommended</para></listItem></list></TD><TD><list class="bullet"><listItem><para>Windows 8.1 and later</para></listItem></list></TD></tr><tr><TD><para><ui>Minimum OS required (one for each platform)</ui></para></TD><TD><para>When  a device does not meet the minimum OS version requirement, it will be reported as non-compliant. A link with information on how to upgrade will be displayed. The end-user can choose to upgrade their device after which they will be able to access company resources.</para></TD><TD><list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>Windows 8.1</para>
                        </listItem>
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                        <listItem>
                          <para>Android 4.0 and later</para>
                        </listItem>
                        <listItem>
                          <para>Samsung KNOX Standard 4.0 and later</para>
                        </listItem>
                      </list></TD></tr><tr><TD><para><ui>Maximum OS version allowed (one for each platform)</ui></para></TD><TD><para>When a device is using an OS version later than the one specified in the rule, access to company resources is blocked and the user is asked to contact their IT admin. Until there is a change in rule to allow the OS version, this device cannot be used to access company resources.</para></TD><TD><list class="bullet">
                        <listItem>
                          <para>Windows Phone 8 and later</para>
                        </listItem>
                        <listItem>
                          <para>Windows 8.1</para>
                        </listItem>
                        <listItem>
                          <para>iOS 6 and later</para>
                        </listItem>
                        <listItem>
                          <para>Android 4.0 and later</para>
                        </listItem>
                        <listItem>
                          <para>Samsung KNOX Standard 4.0 and later</para>
                        </listItem>
                      </list></TD></tr>
                </tbody>
              </table>
              <para>
                <?Comment RS: 153797 2015-04-01T11:07:00Z  Id='1?>
                <superscript>1</superscript> For devices that run Windows and are secured with a Microsoft Account, the compliance policy will fail to evaluate correctly if <ui>Minimum password length</ui> is greater than 8 characters or if <ui>Minimum number of character sets</ui> is more than 2.<?CommentEnd Id='1'
    ?></para>
            </content>
          </step>
          <step>
            <content>
              <para>When you are finished, click <ui>Save Policy</ui>.</para>
            </content>
          </step>
        </steps>
        <conclusion>
          <content>
            <para>The new policy displays in the <ui>Compliance Policies</ui> node of the <ui>Policy</ui> workspace.</para>
          </content>
        </conclusion>
      </procedure>
    </content>
  </section>
  <section>
    <title>Deploy a compliance policy</title>
    <content>
      <para>Deploy the compliance policy to one or more groups of users or devices in your organization.</para>
      <para>For more information about how to deploy policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para>
      <para>Use the status summary and alerts on the <ui>Overview</ui> page of the <ui>Policy</ui> workspace to identify issues with the policy that require your attention. Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</para>
    </content>
  </section>
  <section>
    <title>Monitor the compliance policy</title>
    <content>
      <procedure expanded="true">
        <title>To view devices that do not conform to a compliance policy</title>
        <steps class="ordered">
          <step>
            <content>
              <para>In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Groups</ui>.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Open the <ui>Policy</ui> tab for any device that is compatible with compliance policies.</para>
            </content>
          </step>
          <step>
            <content>
              <para>
                <?Comment RS: Check this is correctConfusion maybe – this might be the GROUPS workspace. 2015-04-03T08:37:00Z  Id='2?>From the <ui>Filters</ui> drop-down list, select <ui>Does not conform to compliance policy</ui>.<?CommentEnd Id='2'
    ?></para>
            </content>
          </step>
        </steps>
      </procedure>
    <procedure>
<title>To view the Health Attestation Reports</title>
 <steps class="ordered">
        <step><content><para>In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Reports</ui>.</para></content></step>
        <step><content><para>In the <ui>Health Attestation Report - Create a new report</ui> page, you can view a report with all the Windows 10 health attestation data collected by Intune. You can also create a report with a subset of the data using filters. The filters can be based on the type of device, operating system, or only a subset of data points. </para></content></step>
      </steps>
</procedure></content>
  </section>
  <section>
    <title>How Intune policy conflicts are resolved</title>
    <content>
      <para>When conflicts occur due to multiple Intune settings being applied to a device, the following rules apply:</para>
      <list class="bullet">
        <listItem>
          <para>If the conflicting settings are from an Intune configuration policy and a compliance policy, the settings in the compliance policy take precedence over the settings in the configuration policy, even if the settings in the configuration policy are more secure.</para>
        </listItem>
        <listItem>
          <para>If you have deployed multiple compliance policies, the most secure of these policies will be used.</para>
        </listItem>
      </list>
    </content>
  </section>
  <nextSteps>
    <content>
      <para>You can now use the compliance policy with conditional access policies to control access to services in your organization.</para>
    </content>
  </nextSteps>
  <relatedTopics>
    <link xlink:href="c564d292-b83b-440d-bf08-3f5b299b7a5e">Manage access to email and SharePoint with Microsoft Intune</link>
  </relatedTopics>
</developerWalkthroughDocument>
