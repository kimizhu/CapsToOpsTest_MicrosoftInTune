---
description: na
search: na
title: Enable access to company resources with Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-17
ms.author: 03258b9b-2cea-4654-ab05-a27214174f4b
capscontentguid: 3dd8dd4e-e165-4d0c-97b7-b3e86ebab909
---
# Enable access to company resources with Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<developerWalkthroughDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>
      <token>wit_firstref</token> <ui>resource access profiles</ui> work together to help your users gain access to the files and resources they need to do their work successfully, wherever they are.</para>
    <para>
      <token>wit_nextref</token> provides the following mobile device policies that help you to accomplish this goal. Click any item in the table for detailed information about how to configure the policy:</para>
  </introduction>
  <section>
    <title>Resource access profiles and supported platforms</title>
    <content>
      <para/>
      <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
        <thead>
          <tr>
            <TD>
              <para>Intune policy</para>
            </TD>
            <TD>
              <para>What it does</para>
            </TD>
            <TD>
              <para>Windows 8.1 and later</para>
            </TD>
            <TD>
              <para>Windows Phone 8.1 and later</para>
            </TD>
            <TD>
              <para>iOS</para>
            </TD>
            <TD>
              <para>Android</para>
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
                <externalLink>
                  <linkText>Certificate Profiles</linkText>
                  <linkUri>https://technet.microsoft.com/library/dn818904.aspx</linkUri>
                </externalLink>
              </para>
            </TD>
            <TD>
              <para>Help secure access to company resources including wireless networks and VPN connections.</para>
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
                <externalLink>
                  <linkText>Wi-Fi Profiles</linkText>
                  <linkUri>https://technet.microsoft.com/library/dn818903.aspx</linkUri>
                </externalLink>
              </para>
            </TD>
            <TD>
              <para>Deploy wireless network settings to your users. By deploying these settings, you minimize the end-user effort required to connect to the corporate network.</para>
            </TD>
            <TD>
              <para>Yes (you can import a Windows Wi-Fi profile)</para>
            </TD>
            <TD>
              <para>Yes (you can configure OMA-URI) <superscript>1</superscript></para>
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
                <externalLink>
                  <linkText>VPN Profiles</linkText>
                  <linkUri>https://technet.microsoft.com/library/dn818905.aspx</linkUri>
                </externalLink>
              </para>
            </TD>
            <TD>
              <para>Deploy Virtual Private Network (VPN) settings to your users. By deploying these settings, you minimize the end-user effort required to connect to resources on the corporate network.</para>
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
                <externalLink>
                  <linkText>Email Profiles</linkText>
                  <linkUri>https://technet.microsoft.com/library/dn800672.aspx</linkUri>
                </externalLink>
              </para>
            </TD>
            <TD>
              <para>Create, deploy and monitor Exchange ActiveSync email settings on devices in your organization.</para>
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
            <TD>
              <para>Yes</para>
            </TD>
          </tr>
        </tbody>
      </table>
      <para>
        <superscript>1</superscript> See <externalLink><linkText>this blog post</linkText><linkUri>http://blogs.technet.com/b/microsoftintune/archive/2015/02/23/using-oma-uri-to-create-custom-wi-fi-profiles-for-windows-phone-8-1.aspx</linkUri></externalLink> for information about how to configure a Windows Phone 8.1 Wi-Fi profile using OMA-URI.</para>
    </content>
  </section>
  <relatedTopics>
    <link xlink:href="7b938d95-c068-4d71-a580-c1492c4bff27">Provision and configure devices with Microsoft Intune</link>
    
    
    
  </relatedTopics>
</developerWalkthroughDocument>
