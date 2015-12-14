---
description: na
keywords: na
pagetitle: Microsoft Intune mobile app management policies and iOS Open In
search: na
ms.author: fb8a7802-3b27-41b8-82f3-31bfdcf49ff2
ms.date: 2015-11-17
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a4515c1-b325-4ac1-9f0a-45ac27e00681
---
# Microsoft Intune mobile app management policies and iOS Open In
Part of protecting your company data requires making sure that file transfers is restricted to apps that are managed by you.   Below are two types of apps that you manage:

- Apps that you are deploying through the MDM solution, which we will refer to as **MDM managed** apps.

- Apps that are associated with mobile application management policies, which we will refer to as **policy-managed**  apps.

In some cases, the platform has built-in features that can be used to manage file transfers between apps. The **Open in management** feature for iOS devices helps restrict file transfers between managed apps. Open in management restrictions are set in configuration profile settings and deployed using your MDM software.  When the user installs the managed app, the restrictions are applied.

Mobile app management (MAM) policies work with **Open in management** to protect company data on iOS devices as described below:

- **BYOD devices not managed by any MDM solution:** You can set the MAM policy settings to **Allow app to transfer data to only managed apps**. When the end-user opens a protected file in an app that is not policy-managed, the file is unreadable.

- **Devices managed by Intune:** You can protect company data transfer between policy-managed apps by using the  **Allow app to transfer data to only managed apps** setting. You can use the **Open in** feature on iOS devices to control data transfer between MDM managed apps.   For devices enrolled in Intune, data transfer between policy-managed apps and MDM managed apps is allowed and configured automatically.

- **Devices managed by a third party MDM:** You can restrict data transfer to only managed apps by using the Open in management feature. However, if you want to make sure that the apps that you have deployed through the third party MDM solution are also protected by the MAM policies, you must use the user UPN setting as described in the [Configure Open in Management with user UPN setting](#bkmk_userUPN) walkthrough.  When apps are deployed with the user UPN setting, the MAM policies are applied to the app when the end-user signs-in using their work account.

> [!IMPORTANT]
> The user UPN setting is only required for apps deployed to devices managed by a third party MDM.  For Intune managed devices, this setting is not required.

## <a name="bkmk_userUPN"></a>Configure Open in Management with user UPN setting
This configuration is required for devices that are managed by a third party MDM. The procedure described below is a general flow on how to implement the UPN setting and the resulting end-user experience:

1. Configure an iOS mobile app management policy. Configure policy settings per your company requirements and associate the policy to Microsoft Office apps.

2. Deploy the Microsoft Office apps (and any other desired apps, email profile) through your third party MDM solution using the setting described in the next two steps.

3. Deploy these apps with the following app configuration settings: key=IntuneMAMUPN, Value=&lt;username@company.com&gt; [example: ‘IntuneMAMUPN’, ‘jondoe@microsoft.com’]

4. Deploy the Open in management policy to enrolled devices.

5. End-user installs the Office apps on the device.

6. End-user launches the managed native email app to access their email.

7. End-user tries to open document from native mail in Microsoft Word.

8. When the Word app launches, the end-user is prompted to log in using their work account.  This account should match the one specified in the configured in the app configuration settings for Microsoft Word.

   > [!NOTE]
   > Then end-user can add other personal accounts to Word to do their personal work.

9. When the login is successful, the app policy settings are applied to the Word app.

10. Now the data transfer succeeds and the document is tagged as corporate identity in the app. In addition, the data is treated in a work context the policy settings are applied accordingly.

## See Also
[Configure data loss prevention app policies with Microsoft Intune](../Topic/Configure_data_loss_prevention_app_policies_with_Microsoft_Intune.md)

