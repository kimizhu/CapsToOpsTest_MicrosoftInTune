---
description: na
keywords: na
pagetitle: Mobile device security policy settings in Microsoft Intune
search: na
ms.date: 2015-10-08
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e5ab3b76-08af-4893-b294-fb6627fdc4c6
ms.author: dbdc710f437843008017318979c6adba
---
# Mobile device security policy settings in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<developerWalkthroughDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <alert class="important">
      <para>
        <token>wit_firstref</token> now features separate configuration policies for each device platform, and these policies contain the most up-to-date settings you can use. You can continue to use the mobile device security policy and any existing deployments will still work. However, you should plan to migrate to the new configuration policies as soon as possible as the mobile device security policy will be removed in the future.</para>
    </alert>
    <para>Use <token>wit_firstref</token> mobile device security policies to configure a wide range of settings that you can deploy to managed devices in your organization. These settings can be used to control the functionality and security of your devices.</para>
    <para>You can create and deploy mobile device security policies for the following device types:</para>
    <list class="bullet">
      <listItem>
        <para>Windows RT 8.1 and enrolled Windows 8.1 devices</para>
      </listItem>
      <listItem>
        <para>Windows RT</para>
      </listItem>
      <listItem>
        <para>Windows Phone 8 and Windows Phone 8.1</para>
      </listItem>
      <listItem>
        <para>iOS</para>
      </listItem>
      <listItem>
        <para>Android and Samsung KNOX</para>
      </listItem>
    </list>
    <alert class="note">
      <para>Some settings are not applicable to some devices. See the table below for a full list of settings you can configure.</para>
    </alert>
  </introduction>
  <section>
    <title>Create a mobile device security policy</title>
    <content>
      <procedure>
        <title/>
        <steps class="ordered">
          <step>
            <content>
              <para>In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Add Policy</ui>.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Click <ui>Common Mobile Device Settings</ui> &gt; <ui>Mobile Device Security</ui>.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Choose whether you want to create a policy that contains recommended settings, or whether you want to create a custom policy, and then click <ui>Create Policy</ui>.</para>
              <alert class="tip">
                <para>Click the information icon next to each setting to view the recommended value for the setting.</para>
              </alert>
              <para>For more information about how to create and deploy policies, see the <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link> topic.</para>
            </content>
          </step>
          <step>
            <content>
              <para>See the <link xlink:href="e5ab3b76-08af-4893-b294-fb6627fdc4c6#BKMK_Settings">Policy settings for mobile devices</link> section in this topic for information about the settings you can configure.</para>
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
            <para>The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</para>
          </content>
        </conclusion>
      </procedure>
    </content>
  </section>
  <section>
    <title>Deploy a mobile device security policy</title>
    <content>
      <procedure>
        <title/>
        <steps class="ordered">
          <step>
            <content>
              <para>Deploy the mobile device security policy to one or more groups of users or devices in your organization.</para>
            </content>
          </step>
        </steps>
        <conclusion>
          <content>
            <para>For more information about how to deploy policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para>
            <para>A status summary and alerts on the <ui>Overview</ui> page of the <ui>Policy</ui> workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</para>
            <alert class="important">
              <para>
                <?Comment RS: 128917 2015-05-06T08:11:00Z  Id='1?>It might take up to 24 hours for status information to appear in the <token>wit_nextref</token> admin console.<?CommentEnd Id='1'
    ?></para>
            </alert>
          </content>
        </conclusion>
      </procedure>
    </content>
  </section>
  <section address="BKMK_Settings" expanded="true">
    <title>Policy settings for mobile devices</title>
    <content>
      <para/>
    </content>
    <sections>
      <section address="BKMK_sec" expanded="true">
        <title>Security settings</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Require a password to unlock mobile devices</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Required password type</ui>
                  </para>
                  <para>(specifies the type of password that will be required, such as numeric only, or alphanumeric)</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Required password type – Minimum number of character sets</ui>
                  </para>
                  <para>There are four character sets, lowercase letters, uppercase letters, numbers, and symbols. This setting specifies how many different character sets must be included in the password). However, for iOS devices, this specifies the number of symbol characters must be included in the password)</para>
                </TD>
                <TD>
                  <para>Yes<superscript>2</superscript></para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Minimum password length</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow simple passwords</ui>
                  </para>
                  <para>Simple passwords include ‘0000’ and ‘1234’</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Number of repeated sign-in failures to allow before the device is wiped</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Minutes of inactivity before screen turns off</ui>
                    <superscript>1</superscript>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Password expiration (days)</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Remember password history</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Remember password history</ui> – <ui>Prevent reuse of previous passwords</ui></para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Password quality</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow picture password and PIN</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Minutes of inactivity before password is required</ui>
                    <superscript>1</superscript>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow fingerprint unlock</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>iOS 7 and later</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <superscript>1</superscript> For iOS devices, when you configure the settings <ui>Minutes of inactivity before screen turns off</ui> and <ui>Minutes of inactivity before password is required</ui>, they are applied in sequence. For example, if you set the value for both settings to <ui>5</ui> minutes, the screen will turn off automatically after 5 minutes, and the device will be locked after an additional 5 minutes. However, if the user turns off the screen manually, the second setting is immediately applied. In the same example, after the user turns off the screen, the device will lock 5 minutes later.</para>
          <para>
            <superscript>2</superscript> When you set deploy a password length policy to devices that run Windows RT, users will be forced to reset their password, even if their current password complies with the policy requirements.</para>
        </content>
      </section>
      <section expanded="true">
        <title>Encryption settings</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Require encryption on mobile device</ui>
                    <superscript>1</superscript>
                  </para>
                  <para>For Windows Phone 8 devices, you must set this to <ui>Yes</ui>.</para>
                  <para>To enable encryption on iOS devices, enable the setting <ui>Require a password to unlock mobile devices</ui>.</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Require encryption on storage cards</ui> <superscript>2</superscript></para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a (apps and associated data are automatically encrypted)</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <superscript>1</superscript> Additional information for devices that run Windows 8.1</para>
          <list class="bullet">
            <listItem>
              <para>To enforce encryption on devices that run Windows 8.1, you must install the <externalLink><linkText>December 2014 MDM client update for Windows</linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> on each device.</para>
            </listItem>
            <listItem>
              <para>If you enable this setting for Windows 8.1 devices, all users of the device must have a Microsoft Account.</para>
            </listItem>
            <listItem>
              <para>For encryption to work, the device must meet the Microsoft <externalLink><linkText>InstantGo</linkText><linkUri>http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/</linkUri></externalLink> hardware certification requirements.</para>
            </listItem>
            <listItem>
              <para>When you enforce encryption on a device, the recovery key is only accessible from the users Microsoft Account, accessed from their OneDrive account. You cannot recover this key on behalf of a user.</para>
            </listItem>
          </list>
          <para>
            <superscript>2</superscript> Applies to devices that are managed by Exchange ActiveSync also.</para>
        </content>
      </section>
      <section expanded="true">
        <title>Malware settings</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Require network firewall</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Enable SmartScreen</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section expanded="true">
        <title>System settings</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Require automatic updates</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Require automatic updates – Minimum classification of updates to install automatically </ui>
                    <superscript>1</superscript>
                  </para>
                  <para>Choose the classification of updates that will be installed automatically:</para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>Important</ui> – Installs all updates classified as important.</para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>Recommended</ui> – Installs all updates classified as important or recommended.</para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow screen capture</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow control center in lock screen</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>iOS 7 and later</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow notification view in lock screen</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>iOS 7 and later</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow today view in lock screen</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>iOS 7 and later</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>User Account Control</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow diagnostic data submission</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow untrusted TLS certificates</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow personal wallet software while locked</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow factory reset</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <superscript>1</superscript> To enforce encryption on devices that run Windows 8.1, you must install the <externalLink><linkText>December 2014 MDM client update for Windows</linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> on each device.</para>
        </content>
      </section>
      <section address="BKMK_cloud" expanded="true">
        <title>Cloud settings – documents and data</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow backup to iCloud</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow document sync to iCloud</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Photo Stream sync to iCloud</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Require encrypted backup</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Work Folders URL</ui>
                  </para>
                  <para>(sets the URL of the work folder to allow documents to be synchronized across devices)</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Google backup</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section expanded="true">
        <title>Cloud settings – accounts and synchronization</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Microsoft account</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Google account auto sync</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_email" expanded="true">
        <title>Email settings</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow users to download email attachments</ui>
                    <superscript>1</superscript>
                  </para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Email synchronization period</ui>
                    <superscript>1</superscript>
                  </para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow mobile devices that don’t fully support these settings to synchronize with Exchange (Exchange ActiveSync)</ui> <superscript>1</superscript></para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
                <TD>
                  <para>n/a</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Make Microsoft account optional in Windows Mail application</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow custom email accounts</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <superscript>1</superscript> Applies to devices that are managed by Exchange ActiveSync also.</para>
        </content>
      </section>
      <section address="BKMK_browser" expanded="true">
        <title>Application settings - browser</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow web browser</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow autofill</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow pop-up blocker</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow cookies</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow plug-ins</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow active scripting</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow fraud warning</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow intranet site for single word entry</ui>
                  </para>
                  <para>(allows use of a single word to direct Internet Explorer to a web site, such as ‘Bing’)</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow automatic detection of intranet network</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Security level for Internet</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Security level for intranet</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Security level for trusted sites</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Security level for restricted sites</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Send Do Not Track header</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Enterprise Mode menu access</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Enterprise Mode site list location</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_apps" expanded="true">
        <title>Application settings - apps</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow application store</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Require a password to access application store</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow in-app purchases</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow managed documents in other unmanaged apps</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>iOS 7 and later</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow unmanaged documents in other managed apps</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>iOS 7 and later</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow video conferencing</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow adult content in media store</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow app installation</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>iOS 6 and later</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section expanded="true">
        <title>Application settings - gaming</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Game Center friends</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow multiplayer gaming</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_hard" expanded="true">
        <title>Device capabilities settings - hardware</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow camera</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow removable storage</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Wi-Fi</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Wi-Fi tethering</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow automatic connection to free Wi-Fi hotspots</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Wi-Fi hotspot reporting</ui>
                  </para>
                  <para>(send information about Wi-Fi connections to help discover nearby connections)</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow geolocation</ui>
                  </para>
                  <para>(allows the device to utilize location information)</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow NFC</ui>
                  </para>
                  <para>(allows operations that use near field communication)</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Bluetooth</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow power off</ui>
                    <superscript>1</superscript>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <superscript>1</superscript> If this setting is disabled, the setting <ui>Number of repeated sign in failures to allow before the device is wiped</ui> for Samsung KNOX devices does not function.</para>
        </content>
      </section>
      <section expanded="true">
        <title>Device capabilities settings - cellular</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow voice roaming</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow data roaming</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow automatic synchronization while roaming</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow SMS/MMS messaging</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section expanded="true">
        <title>Device capabilities settings - features</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Windows 8.1 and Windows RT 8.1</para>
                </TD>
                <TD>
                  <para>Windows RT</para>
                </TD>
                <TD>
                  <para>Windows Phone 8 and Windows Phone 8.1</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow voice assistant</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow voice assistant while device is locked</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow voice dialing</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow copy and paste</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Windows Phone 8.1 only</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow clipboard share between applications</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow YouTube</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes (Samsung KNOX only)</para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
    </sections>
  </section>
  <relatedTopics>
    <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
  </relatedTopics>
</developerWalkthroughDocument>
