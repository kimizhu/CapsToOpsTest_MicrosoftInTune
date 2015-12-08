<?xml version="1.0" encoding="utf-8"?>
<developerWalkthroughDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Use the <token>wit_firstref</token> <ui>Android general configuration policy</ui> to configure settings for:</para>
    <list class="bullet">
      <listItem>
        <para>
          <ui>Mobile device security settings</ui> – Choose from a list of predefined settings that let you control a range of features and functionality on the device.</para>
      </listItem>
      <listItem>
        <para>
          <ui>Kiosk mode</ui> (for Samsung KNOX devices only) - Lock a device to only allow certain features to work. For example, you can allow a device to only run one managed app that you specify, or you can disable the volume buttons on a device. These settings might be used for a demonstration model of a device, or a device that is dedicated to performing only one function, such as a point of sale device.</para>
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
    <title>Create an Android configuration policy</title>
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
              <para>Click <ui>Android</ui> &gt; <ui>General Configuration</ui> and then click <ui>Create Policy</ui>.</para>
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
    <title>Mobile device security policy settings for Android devices</title>
    <content>
      <para>If the setting you are looking for does not appear in this list, you might be able to create it using an Android custom policy that lets you use OMA-URI settings to control the device. For more information, see <link xlink:href="15904440-5a05-47c9-818e-48073b4090e7">Use Android custom policies to manage device settings with Microsoft Intune</link>.</para>
    </content>
    <sections>
      <section address="BKMK_sec" expanded="false">
        <?Comment RS: Done 2015-05-05T14:25:00Z  Id='0?>
        <title>Password settings</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Android 4.0+</para>
                </TD>
                <TD>
                  <para>Samsung KNOX</para>
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
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Minutes of inactivity before screen turns off</ui>
                    
                  </para>
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
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Password quality</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr><tr>
                <TD>
                  <para>
                    <ui>Allow fingerprint unlock</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='0'
    ?>
        </content>
      </section>
      <section expanded="false">
        <?Comment RS: Done 2015-05-05T14:27:00Z  Id='1?>
        <title>Encryption settings</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Android 4.0+</para>
                </TD>
                <TD>
                  <para>Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Require encryption on mobile device</ui>
                  </para>
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
                    <ui>Require encryption on storage cards</ui> </para>
                </TD>
                <TD>
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='1'
    ?>
        </content>
      </section>
      <section expanded="false">
        <?Comment RS: Cone 2015-05-05T14:28:00Z  Id='2?>
        <title>System settings</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Android 4.0+</para>
                </TD>
                <TD>
                  <para>Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
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
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow diagnostic data submission</ui>
                  </para>
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
                    <ui>Allow factory reset</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
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
      <section address="BKMK_cloud" expanded="false">
        <?Comment RS: Done 2015-05-05T14:29:00Z  Id='3?>
        <title>Cloud settings – documents and data</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Android and Samsung KNOX</para>
                </TD>
                <TD>
                  <para>Android 4.0+</para>
                </TD>
              </tr>
            </thead>
            <tbody>
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
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='3'
    ?>
        </content>
      </section>
      <section expanded="false">
        <?Comment RS: Done 2015-05-05T14:36:00Z  Id='4?>
        <title>Cloud settings – accounts and synchronization</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Android 4.0+</para>
                </TD>
                <TD>
                  <para>Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
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
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='4'
    ?>
        </content>
      </section>
      <section address="BKMK_browser" expanded="false">
        <?Comment RS: Done 2015-05-05T14:42:00Z  Id='5?>
        <title>Application settings - browser</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Android 4.0+</para>
                </TD>
                <TD>
                  <para>Samsung KNOX</para>
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
                  <para>No</para>
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
                  <para>No</para>
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
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow active scripting</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
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
      <section address="BKMK_apps" expanded="false">
        <?Comment RS: Done 2015-05-05T14:57:00Z  Id='6?>
        <title>Application settings - apps</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Android 4.0+</para>
                </TD>
                <TD>
                  <para>Samsung KNOX</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow Google Play store</ui>
                  </para>
                </TD>
                <TD>
                  <para>No</para>
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
        <?Comment RS: Done 2015-05-05T14:59:00Z  Id='7?>
        <title>Device capabilities settings - hardware</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Android 4.0+</para>
                </TD>
                <TD>
                  <para>Samsung KNOX</para>
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
                  <para>Yes</para>
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
                  <para>Yes</para>
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
                  <para>Yes</para>
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
                  <para>Yes</para>
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
                  <para>Yes</para>
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
                  <para>Yes</para>
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
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <superscript>1</superscript> If this setting is disabled, the setting <ui>Number of repeated sign in failures to allow before the device is wiped</ui> for Samsung KNOX devices does not function.</para>
          <?CommentEnd Id='7'
    ?>
        </content>
      </section>
      <section expanded="false">
        <?Comment RS: Done 2015-05-05T15:01:00Z  Id='8?>
        <title>Device capabilities settings - cellular</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Android 4.0+</para>
                </TD>
                <TD>
                  <para>Samsung KNOX</para>
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
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
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
        <?Comment RS: Done 2015-05-05T15:02:00Z  Id='9?>
        <title>Device capabilities settings - features</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
                </TD>
                <TD>
                  <para>Android 4.0+</para>
                </TD>
                <TD>
                  <para>Samsung KNOX</para>
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
                  <para>No</para>
                </TD>
                <TD>
                  <para>Yes</para>
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
                <TD>
                  <para>Yes</para>
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
                  <para>Yes</para>
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
      <para>Specify the following settings for <ui>Samsung KNOX devices</ui>:</para>
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
              <para>Click <ui>Browse</ui>, then select the managed app, or app from a store that will be allowed to run when the device is in kiosk mode. No other apps will be allowed to run on the device.</para>
              <para>
                <link xlink:href="ab46be6c-ab73-4c99-8492-66d1dd418293#BKMK_URL">How to specify URLs to app stores</link>
              </para>
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
                <ui>Allow screen sleep wake button</ui>
              </para>
            </TD>
            <TD>
              <para>Enables or disables the screen sleep wake button on the device.</para>
            </TD>
          </tr>
        </tbody>
      </table>
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
            <para>For more information about how to deploy policies, see <?xm-insertion_mark_start author="" time="20150615T094006-0800"?><link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link><?xm-insertion_mark_end?><?xm-deletion_mark author="" time="20150615T094012-0800" data="&lt;maml:link xlink:href=&quot;3deb291f-4bef-49ba-bdc8-974426bab26d&quot; xmlns:maml=&quot;http://ddue.schemas.microsoft.com/authoring/2003/5&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot;&gt;Use policies to manage computers and mobile devices in Microsoft Intune&lt;/maml:link&gt;"?>.</para>
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
          <para>In the <externalLink><linkText>Apps section of Google Play</linkText><linkUri>https://play.google.com/store/apps</linkUri></externalLink>, search for the app you want to use.</para>
          <para>Open the installation page for the app, and copy the URL to the clipboard. You can now use this as the URL in either the compliant or noncompliant apps list.</para>
          <para>
            <ui>Example:</ui> Search Google Play for Microsoft Office Mobile. The URL you use will be <ui>https://play.google.com/store/apps/details?id=com.microsoft.office.officehub</ui>.</para>
        </content>
      </section>
    </sections>
  </section>
  <nextSteps>
    <content>
      <para/>
    </content>
  </nextSteps>
  <relatedTopics>
    <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
  </relatedTopics>
</developerWalkthroughDocument>
