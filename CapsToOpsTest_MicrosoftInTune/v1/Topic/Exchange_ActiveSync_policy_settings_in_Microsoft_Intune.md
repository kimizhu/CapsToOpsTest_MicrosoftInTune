---
description: na
keywords: na
pagetitle: Exchange ActiveSync policy settings in Microsoft Intune
search: na
ms.date: 2015-10-08
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9cbb826-b155-4df6-abf3-60c6f05b2783
ms.author: dbdc710f437843008017318979c6adba
---
# Exchange ActiveSync policy settings in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<developerWalkthroughDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Use the <token>wit_firstref</token> Exchange ActiveSync policy to configure settings that let you control a range of features and functionality on devices that are managed by Exchange ActiveSync.</para>
  </introduction>
  <section>
    <title>Create an Exchange ActiveSync policy</title>
    <content>
      <procedure>
        <title>To provide basic settings for the policy</title>
        <steps class="ordered">
          <step>
            <content>
              <para>In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Overview</ui> &gt; <ui>Add Policy</ui>.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Click <ui>Common Mobile Device Settings</ui> &gt; <ui>Exchange ActiveSync</ui> and then click <ui>Create Policy</ui>.</para>
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
    <title>Policy settings for devices managed by Exchange ActiveSync</title>
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
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Require a password to unlock mobile devices</ui>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Required password type</ui>
                  </para>
                  <para>(specifies the type of password that will be required, such as numeric only, or alphanumeric)</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Minimum password length</ui>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow simple passwords</ui>
                  </para>
                  <para>Simple passwords include ‘0000’ and ‘1234’</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Number of repeated sign-in failures to allow before the device is wiped</ui>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Password expiration (days)</ui>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Remember password history</ui>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Remember password history</ui> – <ui>Prevent reuse of previous passwords</ui></para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Minutes of inactivity before password is required</ui>
                    
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
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
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Require encryption on storage cards</ui> </para>
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
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>Allow users to download email attachments</ui>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Email synchronization period</ui>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Allow mobile devices that don’t fully support Exchange ActiveSync settings to synchronize with Exchange</ui> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_browser" expanded="true">
        <title>Applications - Browser</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
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
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_hard" expanded="true">
        <title>Device capabilities - hardware</title>
        <content>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Setting name</para>
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
              </tr>
            </tbody>
          </table>
        </content>
      </section>
    </sections>
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
            <para>For more information about how to deploy policies, see <?xm-insertion_mark_start author="" time="20150615T100941-0800"?><link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link><?xm-insertion_mark_end?><?xm-deletion_mark author="" time="20150615T100944-0800" data="&lt;maml:link xlink:href=&quot;3deb291f-4bef-49ba-bdc8-974426bab26d&quot; xmlns:maml=&quot;http://ddue.schemas.microsoft.com/authoring/2003/5&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot;&gt;Use policies to manage computers and mobile devices in Microsoft Intune&lt;/maml:link&gt;"?>.</para>
            <para>A status summary and alerts In the <ui>Policy</ui> workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</para>
          </content>
        </conclusion>
      </procedure>
    </content>
  </section>
  <relatedTopics>
    <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
  </relatedTopics>
</developerWalkthroughDocument>
