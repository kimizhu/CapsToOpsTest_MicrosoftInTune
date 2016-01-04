---
description: na
keywords: na
pagetitle: Windows configuration policy settings in Microsoft Intune
search: na
ms.date: 2015-10-08
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6982a2bc-aafa-475a-9236-4840b709e5a1
ms.author: dbdc710f437843008017318979c6adba
---
# Windows configuration policy settings in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<developerWalkthroughDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>Use the <token>wit_firstref</token> <ui>Windows general configuration policy</ui> to configure settings for enrolled Windows 8, and Windows 8.1 devices:</para>
    
  </introduction>
  
  <section>
    <title>Create a Windows general configuration policy</title>
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
              <para>Click <ui>Windows</ui> &gt; <ui>General Configuration (Windows 8.1 and later)</ui> and then click <ui>Create Policy</ui>.</para>
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
  </section><section address="BKMK_Settings" expanded="true">
    <title>Settings for enrolled Windows devices</title>
    <content>
      <para/>
    </content>
    <sections>
      <section address="BKMK_sec" expanded="true">
        <?Comment RS: Done 2015-05-05T14:16:00Z  Id='1?>
        <title>Security settings</title>
        <content>
          <table>
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
              </tr>
            </thead>
            <tbody>
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
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>Minimum password length</ui>
                  <superscript>1</superscript></para>
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
                    <ui>Allow picture password and PIN</ui>
                  </para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
                <TD>
                  <para>Yes</para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <superscript>1</superscript> When you set deploy a password length policy to devices that run Windows RT, users will be forced to reset their password, even if their current password complies with the policy requirements.</para>
          <?CommentEnd Id='1'
    ?>
        </content>
      </section>
      <section expanded="true">
        <?Comment RS: Done 2015-05-05T14:17:00Z  Id='2?>
        <title>Encryption settings</title>
        <content>
          <table>
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
          <?CommentEnd Id='2'
    ?>
        </content>
      </section>
      <section expanded="true">
        <?Comment RS: Done 2015-05-05T14:18:00Z  Id='3?>
        <title>Malware settings</title>
        <content>
          <table>
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
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='3'
    ?>
        </content>
      </section>
      <section expanded="true">
        <?Comment RS: Done 2015-05-05T14:31:00Z  Id='4?>
        <title>System settings</title>
        <content>
          <table>
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
              </tr>
            </tbody>
          </table>
          <para>
            <superscript>1</superscript> To enforce encryption on devices that run Windows 8.1, you must install the <externalLink><linkText>December 2014 MDM client update for Windows</linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> on each device.</para>
          <?CommentEnd Id='4'
    ?>
        </content>
      </section>
      <?Comment RS: Done 2015-05-05T14:37:00Z  Id='5?>
      <section address="BKMK_cloud" expanded="true">
        <title>Cloud settings – documents and data</title>
        <content>
          <table>
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
              </tr>
            </thead>
            <tbody>
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
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='5'
    ?>
        </content>
      </section>
      <?Comment RS: Done 2015-05-05T14:43:00Z  Id='6?>
      <section address="BKMK_email" expanded="true">
        <title>Email settings</title>
        <content>
          <table>
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
              </tr>
            </thead>
            <tbody>
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
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='6'
    ?>
        </content>
      </section>
      <section address="BKMK_browser" expanded="true">
        <?Comment RS: Done 2015-05-05T14:54:00Z  Id='7?>
        <title>Application settings - browser</title>
        <content>
          <table>
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
              </tr>
            </thead>
            <tbody>
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
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='7'
    ?>
        </content>
      </section>
      <section expanded="true">
        <?Comment RS: Done 2015-05-05T14:55:00Z  Id='8?>
        <title>Device capabilities settings - cellular</title>
        <content>
          <table>
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
              </tr>
            </thead>
            <tbody>
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
              </tr>
            </tbody>
          </table>
          <?CommentEnd Id='8'
    ?>
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
            <para>For more information about how to deploy policies, see <?xm-insertion_mark_start author="" time="20150615T094254-0800"?><link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link><?xm-insertion_mark_end?><?xm-deletion_mark author="" time="20150615T094257-0800" data="&lt;maml:link xlink:href=&quot;3deb291f-4bef-49ba-bdc8-974426bab26d&quot; xmlns:maml=&quot;http://ddue.schemas.microsoft.com/authoring/2003/5&quot; xmlns:xlink=&quot;http://www.w3.org/1999/xlink&quot;&gt;Use policies to manage computers and mobile devices in Microsoft Intune&lt;/maml:link&gt;"?>.</para>
            <para>A status summary and alerts in the <ui>Policy</ui> workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</para>
          </content>
        </conclusion>
      </procedure>
    </content>
  </section>
  <relatedTopics>
    <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
  </relatedTopics>
</developerWalkthroughDocument>
