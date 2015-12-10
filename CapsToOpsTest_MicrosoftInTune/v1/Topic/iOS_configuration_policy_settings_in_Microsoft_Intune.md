---
description: na
search: na
title: iOS configuration policy settings in Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-17
ms.author: dbdc710f437843008017318979c6adba
capscontentguid: ab46be6c-ab73-4c99-8492-66d1dd418293
---
# iOS configuration policy settings in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<developerWalkthroughDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Use the <token>wit_firstref</token> <ui>iOS general configuration policy</ui> to configure settings for:</para>
    <list class="bullet">
      <listItem>
        <para>
          <ui>Mobile device security settings</ui> – Choose from a list of predefined settings that let you control a range of features and functionality on the device.</para>
      </listItem>
      <listItem>
        <para>
          <ui>Kiosk mode</ui> - Lock a device to only allow certain features to work. For example, you can allow a device to only run one managed app that you specify, or you can disable the volume buttons on a device. These settings might be used for a demonstration model of a device, or a device that is dedicated to performing only one function, such as a point of sale device.</para>
      </listItem>
      <listItem>
        <para>
          <ui>Compliant and noncompliant apps</ui> - Specify a list of apps that are compliant, or not compliant in your company. On Android and iOS devices, the <ui>Noncompliant Apps Report</ui> can be used to view the compliance of apps you specified in the list against the apps that users have installed (but cannot actually block the installation of the app).</para>
      </listItem>
    </list>
    <alert class="tip">
      <para>You can configure terms and conditions for users to ensure that they acknowledge that apps on their device, including personal apps will be evaluated, and noncompliant apps will either be blocked, or reported as noncompliant. Users must accept these terms and conditions before they can enroll their device and use the company portal to get apps. For more information about using terms and conditions, see <legacyLink xlink:href="ce59fb93-01fd-4822-a57d-45ca7d89843d">Working with terms and conditions policies in Microsoft Intune</legacyLink>.</para>
    </alert>
  </introduction>
  <section>
    <title>Create an iOS general configuration policy</title>
    <content>
      <procedure>
        <title>To provide basic settings for the configuration policy</title>
        <steps class="ordered">
          <step>
            <content>
              <para>In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Overview</ui> &gt; <ui>Add Policy</ui>.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Click <ui>iOS</ui> &gt; <ui>General Configuration</ui> and then click <ui>Create Policy</ui>.</para>
              <alert class="note">
                <para>You cannot create a configuration policy using recommended settings. You must create a custom policy.</para>
              </alert>
            </content>
          </step>
          <step>
            <content>
              <para>In the <ui>General</ui> section of the <ui>Create Policy</ui> page, specify a name and a description for the new policy.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Use the information in the following sections to help you supply settings for the policy.</para>
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
  <section address="BKMK_Settings" expanded="true">
    <title>Settings for iOS devices</title>
    <content>
      <para>If the setting you are looking for does not appear in this list, you might be able to create it using an iOS custom policy that lets you import settings you created using the <externalLink><linkText>Apple Configurator Tool</linkText><linkUri>https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12</linkUri></externalLink>. For more information, see <link xlink:href="04e60d5a-3da6-4943-b6ff-e6a331bcbcfa">Use iOS custom policies to manage device settings with Microsoft Intune</link>.</para>
    </content>
    <sections>
      <section address="BKMK_sec" expanded="false">
        <?Comment RS: Done 2015-05-06T07:38:00Z  Id='1?>
        <title>Security settings</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>iOS</para>
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
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Required password type – Minimum number of character sets</ui>
                  </para>
                  <para>There are four character sets, lowercase letters, uppercase letters, numbers, and symbols. This setting specifies how many different character sets must be included in the password). However, for iOS devices, this specifies the number of symbol characters must be included in the password)</para>
                </TD>
                <TD>
                  <para>Yes</para>
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
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow simple passwords</ui>
                  </para>
                  <para>Simple passwords include ‘0000’ and ‘1234’</para>
                </TD>
                <TD>
                  <para>Yes</para>
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
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Remember password history</ui> – <ui>Prevent reuse of previous passwords</ui></para>
                </TD>
                <TD>
                  <para>Yes</para>
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
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow fingerprint unlock</ui>
                  </para>
                </TD>
                <TD>
                  <para>iOS 7.1 and later</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <superscript>1</superscript> For iOS devices, when you configure the settings <ui>Minutes of inactivity before screen turns off</ui> and <ui>Minutes of inactivity before password is required</ui>, they are applied in sequence. For example, if you set the value for both settings to <ui>5</ui> minutes, the screen will turn off automatically after 5 minutes, and the device will be locked after an additional 5 minutes. However, if the user turns off the screen manually, the second setting is immediately applied. In the same example, after the user turns off the screen, the device will lock 5 minutes later.</para>
          <?CommentEnd Id='1'
    ?>
        </content>
      </section>
      <section expanded="false">
        <?Comment RS: Done 2015-05-06T07:38:00Z  Id='2?>
        <title>System settings</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow screenshot</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow control center in lock screen</ui>
                  </para>
                </TD>
                <TD>
                  <para>iOS 7.1 and later</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow notification view in lock screen</ui>
                  </para>
                </TD>
                <TD>
                  <para>iOS 7.1 and later</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow today view in lock screen</ui>
                  </para>
                </TD>
                <TD>
                  <para>iOS 7.1 and later</para>
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
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow untrusted TLS certificates</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow passbook while locked</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='2'
    ?>
        </content>
      </section>
      <?Comment RS: Done 2015-05-06T07:38:00Z  Id='3?>
      <section address="BKMK_cloud" expanded="false">
        <title>Cloud settings – documents and data</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>iOS</para>
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
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow document sync to iCloud</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Photo Stream sync to iCloud</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Require encrypted backup</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='3'
    ?>
        </content>
      </section>
      <section address="BKMK_browser" expanded="false">
        <?Comment RS: Done 2015-05-06T07:38:00Z  Id='4?>
        <title>Application settings - browser</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Safari</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
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
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow cookies</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Java scripting</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
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
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='4'
    ?>
        </content>
      </section>
      <section address="BKMK_apps" expanded="false">
        <?Comment RS: Done 2015-05-06T07:38:00Z  Id='5?>
        <title>Application settings - apps</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>iOS</para>
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
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Require a password to access application store</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow in-app purchases</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow managed documents in other unmanaged apps</ui>
                  </para>
                </TD>
                <TD>
                  <para>iOS 7.1 and later</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow unmanaged documents in other managed apps</ui>
                  </para>
                </TD>
                <TD>
                  <para>iOS 7.1 and later</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow video conferencing</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow adult content in media store</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='5'
    ?>
        </content>
      </section>
      <section expanded="false">
        <?Comment RS: Done 2015-05-06T07:38:00Z  Id='6?>
        <title>Application settings - Games</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow adding Game Center friends</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow multiplayer gaming</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='6'
    ?>
        </content>
      </section>
      <section address="BKMK_hard" expanded="false">
        <?Comment RS: Done 2015-05-06T07:38:00Z  Id='7?>
        <title>Device capabilities settings - hardware</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>iOS</para>
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
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='7'
    ?>
        </content>
      </section>
      <section expanded="false">
        <?Comment RS: Done 2015-05-06T07:38:00Z  Id='8?>
        <title>Device capabilities settings - cellular</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>iOS</para>
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
                  <para>Yes</para>
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
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow global background fetch while roaming</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='8'
    ?>
        </content>
      </section>
      <section expanded="false">
        <?Comment RS: Done 2015-05-06T07:38:00Z  Id='9?>
        <title>Device capabilities settings - features</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>iOS</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Siri</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Siri while device is locked</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow voice dialing</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
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
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='9'
    ?>
        </content>
      </section>
    </sections>
  </section>
  <section>
    <title>Settings for compliant and noncompliant apps</title>
    <content>
      <para>In the <ui>Compliant &amp; Noncompliant Apps</ui> list, specify a list of compliant or noncompliant apps using the following information:</para>
      <alert class="note">
        <para>A single policy can only contain a list of compliant, or a list of noncompliant apps. You cannot specify both in the same policy.</para>
      </alert>
      <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
        <thead>
          <tr>
            <TD>
              <para>Setting name</para>
            </TD>
            <TD>
              <para>More information</para>
            </TD>
          </tr>
        </thead>
        <tbody>
          <tr>
            <TD>
              <para>
                <ui>Report noncompliance when users install the listed apps</ui>
              </para>
            </TD>
            <TD>
              <para>Lists the apps that are not managed by Intune which users are not allowed to install and run.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Do not report noncompliance when users install the listed apps</ui>
              </para>
            </TD>
            <TD>
              <para>Lists the apps that users are allowed to install. Users cannot install any other apps. Apps that are managed by Intune are automatically allowed.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Add</ui>
              </para>
            </TD>
            <TD>
              <para>Adds an app to the selected list. Specify a name of your choice, optionally the app publisher, and the URL to the app in the app store.</para>
              <para>
                <link xlink:href="ab46be6c-ab73-4c99-8492-66d1dd418293#BKMK_URL">How to specify URLs to app stores</link>
              </para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Import Apps</ui>
              </para>
            </TD>
            <TD>
              <para>Imports a list of apps you have specified in a comma-separated values file. Use the format, application name, publisher, app URL in the file.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Edit</ui>
              </para>
            </TD>
            <TD>
              <para>Let’s you edit the name, publisher and URL of the selected app.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Delete</ui>
              </para>
            </TD>
            <TD>
              <para>Deletes the selected app from the list.</para>
            </TD>
          </tr>
        </tbody>
      </table>
    </content>
  </section>
  <section>
    <title>Kiosk mode settings</title>
    <content>
      <para>Specify the following settings for <ui>iOS devices</ui>:</para>
      <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
        <thead>
          <tr>
            <TD>
              <para>Setting name</para>
            </TD>
            <TD>
              <para>More information</para>
            </TD>
          </tr>
        </thead>
        <tbody>
          <tr>
            <TD>
              <para>
                <ui>Select a managed app that will be allowed to run when the device is in kiosk mode</ui>
              </para>
            </TD>
            <TD>
              <para>Click <ui>Browse</ui>, then specify the managed app, or app from a store that will be allowed to run when the device is in kiosk mode. No other apps will be allowed to run on the device.</para>
              <para>
                <link xlink:href="ab46be6c-ab73-4c99-8492-66d1dd418293#BKMK_URL">How to specify URLs to app stores</link>.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Allow touch</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the touch screen on the device.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Allow screen rotation</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables changing the screen orientation when you rotate the device.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Allow volume buttons</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the use of the volume buttons on the device.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Allow ringer switch</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the ringer (mute) switch on the device.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Allow screen sleep wake button</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the screen sleep wake button on the device.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Allow auto lock</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables automatic locking of the device.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Enable mono audio</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the accessibility setting <ui>Mono audio</ui>.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Enable voice over</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the accessibility setting <ui>VoiceOver</ui> which reads aloud text on the device display.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Enable voice over adjustments</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables voiceover adjustments which let you adjust the VoiceOver function (for example, how fast on-screen text is read aloud).</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Enable zoom</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the <ui>Zoom</ui> accessibility setting which lets you use touch to zoom into the device display.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Enable zoom adjustments</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables zoom adjustments which let you adjust the zoom function.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Enable invert colors</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the <ui>Invert Colors</ui> accessibility setting which adjusts the display to help users with visual impairments.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Enable invert colors adjustments</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables invert colors adjustments which let you adjust the invert colors function.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Enable assistive touch</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the <ui>Assistive Touch</ui> accessibility setting which helps users perform on screen gestures which might be difficult for them to perform.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Enable assistive touch adjustments</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables assistive touch adjustments which let you adjust the assistive touch function.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <ui>Enable speech selection</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the <ui>Speak Selection</ui> accessibility settings which can read aloud the text you select.</para>
            </TD>
          </tr>
        </tbody>
      </table>
      <alert class="note">
        <para>The following notes apply to kiosk mode settings for iOS devices:</para>
        <list class="bullet">
          <listItem>
            <para>Before you can configure an iOS device for kiosk mode, you must use the <externalLink><linkText>Apple Configurator Tool</linkText><linkUri>https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12</linkUri></externalLink> or device enrollment manager to put the device into supervised mode. For more information about the Apple Configurator Tool, see your Apple documentation.</para>
          </listItem>
          <listItem>
            <para>If the iOS app you specify is installed after you deploy the configuration policy, the device will not enter kiosk mode until after it is restarted.</para>
          </listItem>
        </list>
      </alert>
    </content>
  </section>
  <section>
    <title>Deploy the Configuration Policy</title>
    <content>
      <procedure>
        <title/>
        <steps class="ordered">
          <step>
            <content>
              <para>Deploy the configuration policy to one or more groups of users or devices in your organization.</para>
            </content>
          </step>
        </steps>
        <conclusion>
          <content>
            <para>For more information about how to deploy policies, see <?xm-insertion_mark_start author="" time="20150615T093525-0800"?><link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link><?xm-insertion_mark_end?><?xm-deletion_mark author="" time="20150615T093543-0800" data="&lt;maml:link xlink:href=&quot;3deb291f-4bef-49ba-bdc8-974426bab26d&quot; xmlns:maml=&quot;http://ddue.schemas.microsoft.com/authoring/2003/5&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot;&gt;Use policies to manage computers and mobile devices in Microsoft Intune&lt;/maml:link&gt;"?>.</para>
            <para>A status summary and alerts In the <ui>Policy</ui> workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</para>
          </content>
        </conclusion>
      </procedure>
    </content>
  </section>
  <section>
    <title>Reference information for compliant and noncompliant apps</title>
    <content>
      <para/>
    </content>
    <sections>
      <section expanded="false">
        <title>Monitor compliant and noncompliant apps</title>
        <content>
          <para>Use the <ui>Noncompliant Apps Report</ui> to view the compliance of allowed and blocked apps.</para>
          <procedure>
            <title>To run the Noncompliant Apps Report</title>
            <steps class="ordered">
              <step>
                <content>
                  <para>In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Reports</ui> &gt; <ui>Noncompliant Apps Report</ui>.</para>
                </content>
              </step>
              <step>
                <content>
                  <para>Select the device groups that you would like to check, whether you want to check for compliant apps, noncompliant apps, or both, then click <ui>View Report</ui>.</para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_URL" expanded="false">
        <title>How to specify URLs to app stores</title>
        <content>
          <para>To specify an app URL in the compliant and noncompliant apps list, or in the <ui>Select a managed app that will be allowed to run when the device is in kiosk mode</ui> option (iOS only), use the following format:</para>
          <para>Using a search engine, find the app you want to use in the iTunes App Store and open the page for the app.</para>
          <para>Copy the URL of the page and use this as the URL to configure the compliant or noncompliant apps list or the app you want to run in kiosk mode.</para>
          <para>
            <ui>Example:</ui> Search for <userInput>Microsoft Word for iPad</userInput>. The URL you use will be <ui>https://itunes.apple.com/us/app/microsoft-word-for-ipad/id586447913?mt=8</ui>.</para>
          <alert class="note">
            <para>You can also use the iTunes software to find the app and then use the <ui>Copy Link</ui> command to get the app URL.</para>
          </alert>
        </content>
      </section>
    </sections>
  </section>
  <relatedTopics>
    <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
  </relatedTopics>
</developerWalkthroughDocument>
