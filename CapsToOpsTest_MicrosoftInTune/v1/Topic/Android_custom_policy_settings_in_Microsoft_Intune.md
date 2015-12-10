---
description: na
search: na
title: Android custom policy settings in Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-10-08
ms.author: dbdc710f437843008017318979c6adba
capscontentguid: 15904440-5a05-47c9-818e-48073b4090e7
---
# Android custom policy settings in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<developerWalkthroughDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Use the <token>wit_firstref</token> <ui>Android custom configuration policy</ui> to deploy OMA-URI (Open Mobile Alliance Uniform Resource Identifier) settings that can be used to control features on Android devices. These are standard settings that many mobile device manufacturers use to control device features.</para>
    <para>This capability is intended to allow you to deploy Android settings that are not configurable with <token>wit_nextref</token> policies. For information about the settings you can configure with these policies, see <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure security policy for mobile devices in Microsoft Intune</link>.</para>
    <alert class="note">
      <para>Currently, Android custom policies only support configuring Wi-Fi settings for Android devices that include a pre-shared key. See <link xlink:href="15904440-5a05-47c9-818e-48073b4090e7#BKMK_Example">Example: Configure a custom Wi-Fi profile with a pre-shared key</link> to learn how to do this.</para>
    </alert>
  </introduction>
  <section>
    <title>How to create an Android custom policy</title>
    <content>
      <para/>
      <procedure>
        <title/>
        <steps class="ordered">
          <step>
            <content>
              <para>In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Overview</ui> &gt; <ui>Add Policy</ui>.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Configure a policy of the type <ui>Android</ui> &gt; <ui>Custom Configuration</ui>.</para>
              <para>For help creating and deploying policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link>.</para>
              <para>You can only create and deploy a custom policy of this type. Recommended settings are not available.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Use the following table to help you configure the general policy settings:</para>
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
                        <ui>Name</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Enter a unique name for the Android custom policy to help you identify it in the <token>wit_nextref</token> console.</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Description</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Provide a description that gives an overview of the Android custom policy and other relevant information that helps you to locate it.</para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </step>
          <step>
            <content>
              <para>In the <ui>OMA-URI Settings</ui> section, click <ui>Add</ui> to add a setting. You can also edit or delete an existing setting.</para>
            </content>
          </step>
          <step>
            <content>
              <para>In the <ui>Add or Edit OMA-URI Setting</ui> dialog box, specify the following information:</para>
              <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
                <thead>
                  <tr>
                    <TD>
                      <para>Item</para>
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
                        <ui>Setting name</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Enter a unique name for the OMA-URI setting to help you identify it in the list of settings.</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Setting description</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Provide a description that gives an overview of the setting and other relevant information to help you locate it.</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Data type</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Select the date type in which you will specify this OMA-URI setting. Choose from:</para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>String</ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>String (XML)</ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>Date and time</ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>Integer</ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>Floating point</ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>Boolean</ui>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>OMA-URI (case sensitive)</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Specify the OMA-URI you want to supply a setting for.</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Value</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Specify the value to associate with the OMA-URI you specified previously.</para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </step>
          <step>
            <content>
              <para>Click <ui>OK</ui> to save the setting and return to the <ui>Create Policy</ui> page.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Continue to add as many settings as you require. When you are done, click <ui>Save Policy</ui>.</para>
            </content>
          </step>
          <step>
            <content>
              <para>The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</para>
            </content>
          </step>
        </steps>
      </procedure>
    </content>
  </section>
  <section>
    <title>Deploy an Android custom policy</title>
    <content>
      <list class="bullet">
        <listItem>
          <para>Deploy the Android custom policy to one or more groups of users or devices in your organization.</para>
        </listItem>
      </list>
      <para>For help deploying policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para>
      <para>A status summary and alerts on the <ui>Overview</ui> page of the <ui>Policy</ui> workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</para>
    </content>
  </section>
  <section address="BKMK_Example">
    <title>Example: Configure a custom Wi-Fi profile with a pre-shared key</title>
    <content>
      <para>Although <token>wit_nextref</token> supports Wi-Fi profiles for Android devices, this feature does not currently support the inclusion of a pre-shared key in the configuration. In this example, you’ll learn how to create an Android custom policy that creates a Wi-Fi profile with a pre-shared key on the Android device.</para>
      <procedure>
        <title>To create a Wi-Fi profile with a pre-shared key</title>
        <steps class="ordered">
          <step>
            <content>
              <para>Ensure that your users are using the latest version of the <externalLink><linkText>Intune Company Portal</linkText><linkUri>https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal</linkUri></externalLink> app for Android.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Create an Android custom policy and add the following OMA-URI setting:</para>
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
                        <ui>Setting name</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Specify a name of your choice for the setting.</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Setting description</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Specify a description for the setting.</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Data type</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Select <ui>String (XML)</ui>.</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>OMA-<?Comment RS: To be decided. 2015-04-07T14:00:00Z  Id='0?>URI<?CommentEnd Id='0'
    ?></ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Enter:</para>
                      <code>./Vendor/MSFT/WiFi/Profile/<placeholder>&lt;Wi-Fi profile&gt;</placeholder>/Settings
</code>
                      <para>Where <placeholder>&lt;Wi-Fi profile&gt;</placeholder> is a unique name for the profile.</para>
                      <para>
                        <ui>Example:</ui> </para>
                      <code>./Vendor/MSFT/WiFi/Profile/ContosoWiFi/Settings
</code>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>Value</ui>
                      </para>
                    </TD>
                    <TD>
                      <para>Copy and paste the following XML code:</para>
                      <code>&lt;!--
WEP Wifi Profile
                <placeholder>&lt;Name of wifi profile&gt;</placeholder> = Name of profile 
                <placeholder>&lt;SSID of wifi profile&gt;</placeholder> = Plain text of SSID. Does not need to be escaped, could be &lt;name&gt;Your Company's Network&lt;/name&gt;
                <placeholder>&lt;WEP password&gt;</placeholder> = Password to connect to the network
--&gt;
&lt;WLANProfile 
xmlns="http://www.microsoft.com/networking/WLAN/profile/v1"&gt;
  &lt;name&gt;<placeholder>&lt;Name of wifi profile&gt;</placeholder>&lt;/name&gt;
  &lt;SSIDConfig&gt;
    &lt;SSID&gt;
      &lt;name&gt;<placeholder>&lt;SSID of wifi profile&gt;</placeholder>&lt;/name&gt;
    &lt;/SSID&gt;
  &lt;/SSIDConfig&gt;
  &lt;connectionType&gt;ESS&lt;/connectionType&gt;
  &lt;MSM&gt;
    &lt;security&gt;
      &lt;authEncryption&gt;
        &lt;authentication&gt;open&lt;/authentication&gt;
        &lt;encryption&gt;WEP&lt;/encryption&gt;
        &lt;useOneX&gt;false&lt;/useOneX&gt;
      &lt;/authEncryption&gt;
      &lt;sharedKey&gt;
        &lt;keyType&gt;networkKey&lt;/keyType&gt;
        &lt;protected&gt;false&lt;/protected&gt;
        &lt;keyMaterial&gt;<placeholder>&lt;WEP password&gt;</placeholder>&lt;/keyMaterial&gt;
      &lt;/sharedKey&gt;
      &lt;keyIndex&gt;0&lt;/keyIndex&gt;
    &lt;/security&gt;
  &lt;/MSM&gt;
&lt;/WLANProfile&gt;</code>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </step>
          <step>
            <content>
              <para>When you are done, save the policy and deploy it to the required Android devices. The new Wi-Fi profile will appear in the list of connections on the device.</para>
            </content>
          </step>
        </steps>
      </procedure>
    </content>
  </section>
  <relatedTopics>
    <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
  </relatedTopics>
</developerWalkthroughDocument>
